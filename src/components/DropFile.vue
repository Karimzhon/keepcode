<template>
    <div class="main-upload">
        <div
            class="dropzone-container"
            @dragover="dragover"
            @dragleave="dragleave"
            @drop="drop"
        >
            <input
                type="file"
                name="file"
                id="fileInput"
                class="hidden-input"
                @change="onChange"
                ref="file"
                accept=".pdf,.jpg,.jpeg,.png"
            />

            <label for="fileInput" class="file-label">
                <div v-if="isDragging">Release to drop files here.</div>
                <div v-else>
                    <u>Выберите файл </u>
                    или перетащите его сюда
                </div>
            </label>
            <div class="preview-container mt-4" v-if="file">
                <div>
                    <p>
                        {{ file.name }} -
                        {{ Math.round(file.size / 1000) + "kb" }}
                    </p>
                </div>
                <div>
                    <button
                        class="ml-2"
                        type="button"
                        @click="remove()"
                        title="Remove file"
                    >
                        <b>×</b>
                    </button>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "DropFile",
    data() {
        return {
            isDragging: false,
            file: '',
        };
    },
    methods: {
        onChange() {
            this.file = this.$refs.file.files[0];
            this.generateURL(this.file)
        },
        dragover(e) {
            e.preventDefault();
            this.isDragging = true;
        },
        dragleave() {
            this.isDragging = false;
        },
        drop(e) {
            e.preventDefault();
            this.$refs.file.files = e.dataTransfer.files;
            this.onChange();
            this.isDragging = false;
            this.generateURL(this.file)
        },
        remove() {
            this.file = '';
            this.generateURL(this.file)
        },
        generateURL(file) {
            let fileSrc, type;
            if (file) {
                fileSrc = URL.createObjectURL(file);
                type = file.type.split('/').pop();
            } else {
                fileSrc = file
            }
            this.$emit("getFile", fileSrc, type)
            return fileSrc;
        },
    },
}
</script>

<style scoped lang="scss">
.main-upload {
    display         : flex;
    flex-grow       : 1;
    align-items     : center;
    justify-content : center;
    text-align      : center;
}

.dropzone-container {
    padding       : 4rem;
    background    : #f2f5f8;
    border        : 1px solid #b9c2c9;
    width         : 100%;
    border-radius : 10px;
    margin-bottom : 50px;
}

.hidden-input {
    opacity  : 0;
    overflow : hidden;
    position : absolute;
    width    : 1px;
    height   : 1px;
}

.file-label {
    display     : block;
    cursor      : pointer;
    font-weight : 400;
    font-size   : 18px;
    line-height : 22px;
    color       : #86939C;

    u {
        text-decoration-line : underline;
    }
}
</style>