<template>
    <div class="documents">
        <a class="documents_item" target="_blank" v-for="item in items" :href="item.file">
            <div class="documents_item_left">
                <p class="item_title">
                    {{ item.title }}
                    <span v-if="item.number">№ {{ item.number }}</span>
                </p>
                <p class="item_status">{{ item.status }}</p>
                <p class="item_date">
                    <span class="item_date_start">{{ item.date_start }}</span>
                    <span class="item_date_start" v-if="item.date_end"> - {{ item.date_end }}</span>
                </p>
                <div class="item_icons">
                    <svg width="25" height="25" viewBox="0 0 25 25" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <g clip-path="url(#clip0_92_87)">
                            <path
                                d="M21.3379 6.29883H20.6543V3.66211C20.6543 1.64282 19.0115 0 16.9922 0H8.00781C5.98853 0 4.3457 1.64282 4.3457 3.66211V6.29883H3.66211C1.64282 6.29883 0 7.94165 0 9.96094V15.8203C0 17.8396 1.64282 19.4824 3.66211 19.4824H4.3457V22.8027C4.3457 24.0143 5.3314 25 6.54297 25H18.457C19.6686 25 20.6543 24.0143 20.6543 22.8027V19.4824H21.3379C23.3572 19.4824 25 17.8396 25 15.8203V9.96094C25 7.94165 23.3572 6.29883 21.3379 6.29883ZM5.81055 3.66211C5.81055 2.45054 6.79624 1.46484 8.00781 1.46484H16.9922C18.2038 1.46484 19.1895 2.45054 19.1895 3.66211V6.29883H5.81055V3.66211ZM19.1895 22.8027C19.1895 23.2066 18.8609 23.5352 18.457 23.5352H6.54297C6.13911 23.5352 5.81055 23.2066 5.81055 22.8027V15.5762H19.1895V22.8027ZM23.5352 15.8203C23.5352 17.0319 22.5495 18.0176 21.3379 18.0176H20.6543V15.5762H21.0938C21.4982 15.5762 21.8262 15.2482 21.8262 14.8438C21.8262 14.4393 21.4982 14.1113 21.0938 14.1113H3.90625C3.50176 14.1113 3.17383 14.4393 3.17383 14.8438C3.17383 15.2482 3.50176 15.5762 3.90625 15.5762H4.3457V18.0176H3.66211C2.45054 18.0176 1.46484 17.0319 1.46484 15.8203V9.96094C1.46484 8.74936 2.45054 7.76367 3.66211 7.76367H21.3379C22.5495 7.76367 23.5352 8.74936 23.5352 9.96094V15.8203Z"
                                fill="#86939C"/>
                            <path
                                d="M14.4531 17.2363H10.5469C10.1424 17.2363 9.81445 17.5643 9.81445 17.9688C9.81445 18.3732 10.1424 18.7012 10.5469 18.7012H14.4531C14.8576 18.7012 15.1855 18.3732 15.1855 17.9688C15.1855 17.5643 14.8576 17.2363 14.4531 17.2363Z"
                                fill="#86939C"/>
                            <path
                                d="M14.4531 20.3613H10.5469C10.1424 20.3613 9.81445 20.6893 9.81445 21.0938C9.81445 21.4982 10.1424 21.8262 10.5469 21.8262H14.4531C14.8576 21.8262 15.1855 21.4982 15.1855 21.0938C15.1855 20.6893 14.8576 20.3613 14.4531 20.3613Z"
                                fill="#86939C"/>
                            <path
                                d="M6.25 9.42383H3.90625C3.50176 9.42383 3.17383 9.75176 3.17383 10.1562C3.17383 10.5607 3.50176 10.8887 3.90625 10.8887H6.25C6.65449 10.8887 6.98242 10.5607 6.98242 10.1562C6.98242 9.75176 6.65449 9.42383 6.25 9.42383Z"
                                fill="#86939C"/>
                        </g>
                        <defs>
                            <clipPath id="clip0_92_87">
                                <rect width="25" height="25" fill="white"/>
                            </clipPath>
                        </defs>
                    </svg>
                    <svg width="25" height="25" viewBox="0 0 25 25" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <g clip-path="url(#clip0_92_72)">
                            <path
                                d="M23.0484 15.6889C22.7028 15.6889 22.2806 15.969 22.2806 16.3147V21.8708C22.2806 22.6566 21.5203 23.4632 20.6874 23.464L3.12887 23.464C2.38222 23.4473 1.53695 22.6801 1.53573 21.8708V5.56379C1.53664 4.7939 2.32738 4.0071 3.12887 4.00617L8.68505 4.00619C9.0307 4.00619 9.31082 3.58395 9.31082 3.23832C9.31082 2.89293 9.0307 2.43494 8.68505 2.43494L3.12887 2.43495C1.40163 2.43691 0.00195534 3.83659 0 5.56382V21.8711C0.00195534 23.5983 1.40163 24.998 3.12887 25H20.6874C22.4147 24.998 23.8144 23.5983 23.8163 21.8711V16.3147C23.8163 15.969 23.3941 15.6889 23.0484 15.6889H23.0485L23.0484 15.6889Z"
                                fill="#86939C"/>
                            <path
                                d="M23.5687 0.824805C22.469 -0.274935 20.686 -0.274935 19.5863 0.824805L8.42205 11.989C8.34554 12.0655 8.29029 12.1604 8.26146 12.2645L6.79334 17.5647C6.73297 17.7821 6.79432 18.0148 6.9537 18.1744C7.11331 18.3338 7.34603 18.3951 7.56335 18.335L12.8636 16.8666C12.9677 16.8378 13.0626 16.7825 13.1391 16.706L24.303 5.54158C25.4011 4.4411 25.4011 2.6596 24.303 1.5591L23.5687 0.824805ZM9.78559 12.3958L18.9226 3.25848L21.8694 6.20525L12.7321 15.3425L9.78561 12.3958H9.78559ZM9.19697 13.5769L11.5512 15.9314L8.29473 16.8336L9.19697 13.5769ZM23.4182 4.65669L22.7545 5.32035L19.8075 2.37335L20.4714 1.70968C21.0823 1.09883 22.0728 1.09883 22.6836 1.70968L23.4182 2.44398C24.0281 3.05559 24.0281 4.04533 23.4182 4.65669Z"
                                fill="#86939C"/>
                        </g>
                        <defs>
                            <clipPath id="clip0_92_72">
                                <rect width="25" height="25" fill="white"/>
                            </clipPath>
                        </defs>
                    </svg>
                    <svg width="25" height="25" viewBox="0 0 25 25" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path
                            d="M12.5 21.5401C12.9045 21.5401 13.2324 21.2122 13.2324 20.8077V10.9733C13.2324 10.5688 12.9045 10.2409 12.5 10.2409C12.0955 10.2409 11.7676 10.5688 11.7676 10.9733V20.8077C11.7676 21.2122 12.0955 21.5401 12.5 21.5401Z"
                            fill="#86939C"/>
                        <path
                            d="M8.46707 20.8766C8.50515 21.28 8.86331 21.5749 9.26511 21.5369C9.66785 21.4988 9.96345 21.1415 9.92542 20.7388L8.9968 10.9044C8.95877 10.5017 8.60213 10.206 8.19876 10.2441C7.79602 10.2821 7.50041 10.6394 7.53845 11.0421L8.46707 20.8766Z"
                            fill="#86939C"/>
                        <path
                            d="M15.7339 21.5369C16.1362 21.575 16.4939 21.2796 16.532 20.8766L17.4606 11.0422C17.4986 10.6395 17.203 10.2822 16.8003 10.2441C16.3969 10.2059 16.0403 10.5018 16.0022 10.9044L15.0736 20.7389C15.0356 21.1416 15.3312 21.4989 15.7339 21.5369Z"
                            fill="#86939C"/>
                        <path
                            d="M2.81445 8.24585H3.25229L5.37378 24.3632C5.42173 24.7276 5.73237 25 6.09995 25H18.8995C19.2671 25 19.5777 24.7276 19.6257 24.3632L21.7472 8.24585H22.185C22.5895 8.24585 22.9174 7.91792 22.9174 7.51343V4.30889C22.9174 3.90439 22.5895 3.57646 22.185 3.57646H15.9176V3.28784C15.9176 1.47495 14.4426 0 12.6297 0H12.3697C10.5568 0 9.08188 1.47495 9.08188 3.28784V3.57646H2.81445C2.40996 3.57646 2.08203 3.90439 2.08203 4.30889V7.51343C2.08203 7.91792 2.40991 8.24585 2.81445 8.24585ZM18.2572 23.5352H6.74224L4.72978 8.24585H20.2697L18.2572 23.5352ZM10.5467 3.28784C10.5467 2.28267 11.3645 1.46484 12.3697 1.46484H12.6297C13.6349 1.46484 14.4527 2.28267 14.4527 3.28784V3.57646H10.5467V3.28784ZM3.54688 5.04131H21.4526V6.78101C21.296 6.78101 3.74219 6.78101 3.54688 6.78101V5.04131Z"
                            fill="#86939C"/>
                    </svg>
                </div>
            </div>
            <div class="documents_item_right">
                <img :src="'/src/assets/' + getType(item.file) + '.svg'" :alt="getType(item.file)">
            </div>
        </a>
        <a class="documents_item" target="_blank" v-for="item in new_items" :href="item.file">
            <div class="documents_item_left">
                <p class="item_title">
                    {{ item.title }}
                    <span v-if="item.number">№ {{ item.number }}</span>
                </p>
                <p class="item_status">{{ item.status }}</p>
                <p class="item_date">
                    <span class="item_date_start">{{ item.date_start }}</span>
                    <span class="item_date_start" v-if="item.date_end"> - {{ item.date_end }}</span>
                </p>
                <div class="item_icons">
                    <svg width="25" height="25" viewBox="0 0 25 25" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <g clip-path="url(#clip0_92_87)">
                            <path
                                d="M21.3379 6.29883H20.6543V3.66211C20.6543 1.64282 19.0115 0 16.9922 0H8.00781C5.98853 0 4.3457 1.64282 4.3457 3.66211V6.29883H3.66211C1.64282 6.29883 0 7.94165 0 9.96094V15.8203C0 17.8396 1.64282 19.4824 3.66211 19.4824H4.3457V22.8027C4.3457 24.0143 5.3314 25 6.54297 25H18.457C19.6686 25 20.6543 24.0143 20.6543 22.8027V19.4824H21.3379C23.3572 19.4824 25 17.8396 25 15.8203V9.96094C25 7.94165 23.3572 6.29883 21.3379 6.29883ZM5.81055 3.66211C5.81055 2.45054 6.79624 1.46484 8.00781 1.46484H16.9922C18.2038 1.46484 19.1895 2.45054 19.1895 3.66211V6.29883H5.81055V3.66211ZM19.1895 22.8027C19.1895 23.2066 18.8609 23.5352 18.457 23.5352H6.54297C6.13911 23.5352 5.81055 23.2066 5.81055 22.8027V15.5762H19.1895V22.8027ZM23.5352 15.8203C23.5352 17.0319 22.5495 18.0176 21.3379 18.0176H20.6543V15.5762H21.0938C21.4982 15.5762 21.8262 15.2482 21.8262 14.8438C21.8262 14.4393 21.4982 14.1113 21.0938 14.1113H3.90625C3.50176 14.1113 3.17383 14.4393 3.17383 14.8438C3.17383 15.2482 3.50176 15.5762 3.90625 15.5762H4.3457V18.0176H3.66211C2.45054 18.0176 1.46484 17.0319 1.46484 15.8203V9.96094C1.46484 8.74936 2.45054 7.76367 3.66211 7.76367H21.3379C22.5495 7.76367 23.5352 8.74936 23.5352 9.96094V15.8203Z"
                                fill="#86939C"/>
                            <path
                                d="M14.4531 17.2363H10.5469C10.1424 17.2363 9.81445 17.5643 9.81445 17.9688C9.81445 18.3732 10.1424 18.7012 10.5469 18.7012H14.4531C14.8576 18.7012 15.1855 18.3732 15.1855 17.9688C15.1855 17.5643 14.8576 17.2363 14.4531 17.2363Z"
                                fill="#86939C"/>
                            <path
                                d="M14.4531 20.3613H10.5469C10.1424 20.3613 9.81445 20.6893 9.81445 21.0938C9.81445 21.4982 10.1424 21.8262 10.5469 21.8262H14.4531C14.8576 21.8262 15.1855 21.4982 15.1855 21.0938C15.1855 20.6893 14.8576 20.3613 14.4531 20.3613Z"
                                fill="#86939C"/>
                            <path
                                d="M6.25 9.42383H3.90625C3.50176 9.42383 3.17383 9.75176 3.17383 10.1562C3.17383 10.5607 3.50176 10.8887 3.90625 10.8887H6.25C6.65449 10.8887 6.98242 10.5607 6.98242 10.1562C6.98242 9.75176 6.65449 9.42383 6.25 9.42383Z"
                                fill="#86939C"/>
                        </g>
                        <defs>
                            <clipPath id="clip0_92_87">
                                <rect width="25" height="25" fill="white"/>
                            </clipPath>
                        </defs>
                    </svg>
                    <svg width="25" height="25" viewBox="0 0 25 25" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <g clip-path="url(#clip0_92_72)">
                            <path
                                d="M23.0484 15.6889C22.7028 15.6889 22.2806 15.969 22.2806 16.3147V21.8708C22.2806 22.6566 21.5203 23.4632 20.6874 23.464L3.12887 23.464C2.38222 23.4473 1.53695 22.6801 1.53573 21.8708V5.56379C1.53664 4.7939 2.32738 4.0071 3.12887 4.00617L8.68505 4.00619C9.0307 4.00619 9.31082 3.58395 9.31082 3.23832C9.31082 2.89293 9.0307 2.43494 8.68505 2.43494L3.12887 2.43495C1.40163 2.43691 0.00195534 3.83659 0 5.56382V21.8711C0.00195534 23.5983 1.40163 24.998 3.12887 25H20.6874C22.4147 24.998 23.8144 23.5983 23.8163 21.8711V16.3147C23.8163 15.969 23.3941 15.6889 23.0484 15.6889H23.0485L23.0484 15.6889Z"
                                fill="#86939C"/>
                            <path
                                d="M23.5687 0.824805C22.469 -0.274935 20.686 -0.274935 19.5863 0.824805L8.42205 11.989C8.34554 12.0655 8.29029 12.1604 8.26146 12.2645L6.79334 17.5647C6.73297 17.7821 6.79432 18.0148 6.9537 18.1744C7.11331 18.3338 7.34603 18.3951 7.56335 18.335L12.8636 16.8666C12.9677 16.8378 13.0626 16.7825 13.1391 16.706L24.303 5.54158C25.4011 4.4411 25.4011 2.6596 24.303 1.5591L23.5687 0.824805ZM9.78559 12.3958L18.9226 3.25848L21.8694 6.20525L12.7321 15.3425L9.78561 12.3958H9.78559ZM9.19697 13.5769L11.5512 15.9314L8.29473 16.8336L9.19697 13.5769ZM23.4182 4.65669L22.7545 5.32035L19.8075 2.37335L20.4714 1.70968C21.0823 1.09883 22.0728 1.09883 22.6836 1.70968L23.4182 2.44398C24.0281 3.05559 24.0281 4.04533 23.4182 4.65669Z"
                                fill="#86939C"/>
                        </g>
                        <defs>
                            <clipPath id="clip0_92_72">
                                <rect width="25" height="25" fill="white"/>
                            </clipPath>
                        </defs>
                    </svg>
                    <svg width="25" height="25" viewBox="0 0 25 25" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path
                            d="M12.5 21.5401C12.9045 21.5401 13.2324 21.2122 13.2324 20.8077V10.9733C13.2324 10.5688 12.9045 10.2409 12.5 10.2409C12.0955 10.2409 11.7676 10.5688 11.7676 10.9733V20.8077C11.7676 21.2122 12.0955 21.5401 12.5 21.5401Z"
                            fill="#86939C"/>
                        <path
                            d="M8.46707 20.8766C8.50515 21.28 8.86331 21.5749 9.26511 21.5369C9.66785 21.4988 9.96345 21.1415 9.92542 20.7388L8.9968 10.9044C8.95877 10.5017 8.60213 10.206 8.19876 10.2441C7.79602 10.2821 7.50041 10.6394 7.53845 11.0421L8.46707 20.8766Z"
                            fill="#86939C"/>
                        <path
                            d="M15.7339 21.5369C16.1362 21.575 16.4939 21.2796 16.532 20.8766L17.4606 11.0422C17.4986 10.6395 17.203 10.2822 16.8003 10.2441C16.3969 10.2059 16.0403 10.5018 16.0022 10.9044L15.0736 20.7389C15.0356 21.1416 15.3312 21.4989 15.7339 21.5369Z"
                            fill="#86939C"/>
                        <path
                            d="M2.81445 8.24585H3.25229L5.37378 24.3632C5.42173 24.7276 5.73237 25 6.09995 25H18.8995C19.2671 25 19.5777 24.7276 19.6257 24.3632L21.7472 8.24585H22.185C22.5895 8.24585 22.9174 7.91792 22.9174 7.51343V4.30889C22.9174 3.90439 22.5895 3.57646 22.185 3.57646H15.9176V3.28784C15.9176 1.47495 14.4426 0 12.6297 0H12.3697C10.5568 0 9.08188 1.47495 9.08188 3.28784V3.57646H2.81445C2.40996 3.57646 2.08203 3.90439 2.08203 4.30889V7.51343C2.08203 7.91792 2.40991 8.24585 2.81445 8.24585ZM18.2572 23.5352H6.74224L4.72978 8.24585H20.2697L18.2572 23.5352ZM10.5467 3.28784C10.5467 2.28267 11.3645 1.46484 12.3697 1.46484H12.6297C13.6349 1.46484 14.4527 2.28267 14.4527 3.28784V3.57646H10.5467V3.28784ZM3.54688 5.04131H21.4526V6.78101C21.296 6.78101 3.74219 6.78101 3.54688 6.78101V5.04131Z"
                            fill="#86939C"/>
                    </svg>
                </div>
            </div>
            <div class="documents_item_right">
                <img :src="'/src/assets/' + new_file_type + '.svg'" :alt="new_file_type">
            </div>
        </a>
    </div>
    <div id="modal">
        <div class="backdrop" @click="closeModal()"></div>
        <div class="modal">
            <div class="modal_header">
                <p class="modal_title">
                    Добавить документ
                </p>
                <svg @click="closeModal()" width="18" height="18" viewBox="0 0 18 18" fill="none"
                     xmlns="http://www.w3.org/2000/svg">
                    <g clip-path="url(#clip0_132_14620)">
                        <path
                            d="M17.3916 3.54608L11.9377 9.00054L17.3916 14.4547C18.2028 15.2663 18.2028 16.5809 17.3916 17.3924C16.9863 17.7978 16.4548 18.0006 15.9237 18.0006C15.3916 18.0006 14.8602 17.7981 14.4551 17.3924L9.00004 11.9376L3.54536 17.3924C3.14008 17.7977 2.6086 18.0005 2.07697 18.0005C1.5455 18.0005 1.01439 17.798 0.608741 17.3924C-0.2025 16.5812 -0.2025 15.2665 0.608741 14.4547L6.06249 9.00049L0.608431 3.54608C-0.20281 2.73485 -0.20281 1.41993 0.608431 0.608696C1.41952 -0.201922 2.73365 -0.201922 3.54505 0.608696L8.99998 6.06315L14.4545 0.608696C15.2661 -0.201922 16.5804 -0.201922 17.3913 0.608696C18.2028 1.41993 18.2028 2.73485 17.3916 3.54608Z"
                            fill="#86939C"/>
                    </g>
                    <defs>
                        <clipPath id="clip0_132_14620">
                            <rect width="18" height="18" fill="white"/>
                        </clipPath>
                    </defs>
                </svg>
            </div>
            <div class="modal_body">
                <div class="modal_type">
                    <div class="left">
                        Тип документа: <span>*</span>
                    </div>
                    <div class="modal_type_inputs">
                        <label>
                            <input type="radio" name="type" value="Договор" v-model="new_item.type">
                            Договор
                        </label>
                        <label>
                            <input type="radio" name="type" value="Справка" v-model="new_item.type">
                            Справка
                        </label>
                        <label>
                            <input type="radio" name="type" value="Другое" v-model="new_item.type">
                            Другое
                        </label>
                    </div>
                </div>
                <span class="error" v-if="type_error">{{ type_error }}</span>
                <div class="document_title">
                    <input class="document_input" type="text" placeholder="Название документа *"
                           v-model="new_item.title">
                    <span class="error" v-if="title_error">{{ title_error }}</span>
                </div>
                <div class="document_title">
                    <input class="document_input" type="text" placeholder="Номер"
                           v-model="new_item.number">
                </div>
                <div class="document_date">
                    <div class="document_date_item">
                        Действует с:
                        <vue-date-picker class="filters_item" placeholder="Не выбрано" auto-apply format="dd.MM.yyyy"
                                         v-model="new_item.date_start" :enable-time-picker="false"></vue-date-picker>
                    </div>
                    <div class="document_date_item">
                        по:
                        <vue-date-picker class="filters_item" placeholder="Не выбрано" auto-apply format="dd.MM.yyyy"
                                         v-model="new_item.date_end" :enable-time-picker="false"></vue-date-picker>
                    </div>
                </div>
                <div class="document_checkbox" :class="{active: checkbox1}">
                    <label>
                        <input type="checkbox" v-model="checkbox1" hidden>
                        Оповещать об окончании
                    </label>
                </div>
                <div class="document_checkbox" :class="{active: checkbox2}">
                    <label>
                        <input type="checkbox" v-model="checkbox2" hidden>
                        Создавать задачу при окончании
                    </label>
                </div>
                <drop-file @getFile="getFile" :key="key_file"></drop-file>
                <div class="modal-footer">
                    <div class="add-elem" @click="addElem()">добавить документ</div>
                    <div class="close_modal" @click="closeModal()">отмена</div>
                </div>
                <pre>
                    {{ new_item }}
                </pre>
            </div>
        </div>
    </div>
</template>

<script>
import VueDatePicker from '@vuepic/vue-datepicker';
import DropFile from "./DropFile.vue";
import '@vuepic/vue-datepicker/dist/main.css'

export default {
    name: "Documents",
    components: {
        VueDatePicker,
        DropFile
    },
    props: {
        filter: Object
    },
    data() {
        return {
            items: [],
            new_items: [],
            new_item: {
                type: null,
                title: null,
                number: null,
                date_start: null,
                date_end: null,
                file: null
            },
            title_error: '',
            new_file_type: null,
            type_error: '',
            checkbox1: false,
            checkbox2: false,
            key_file: null
        }
    },
    mounted() {
        this.getItems()
    },
    methods: {
        getItems() {
            let this_ = this;
            let type = this.filter.type != null ? 'type=' + this.filter.type + '&' : '';
            let status = this.filter.status != null ? 'status=' + this.filter.status : '';
            let value = type + status;
            this.items = [];
            fetch('https://my-json-server.typicode.com/karimzhon/JsonTest/items?' + value)
                .then((response) => response.json())
                .then((data) => {
                    data.filter((resp) => {
                        let split = resp.date_start.split('.')
                        let time = [split[1], split[0], split[2]].join('/')
                        if (new Date(time).getTime() > new Date(this.filter.date).getTime()) {
                            this_.items.push(resp);
                        }
                    })
                })
        },
        /*async setItems() {
            const url = 'https://my-json-server.typicode.com/karimzhon/JsonTest/items';
            const data = {
                id: 2,
                title: 'example'
            };

            try {
                const response = await fetch(url, {
                    method: 'POST',
                    body: JSON.stringify(data),
                    headers: {
                        'Content-Type': 'application/json'
                    }
                });
                const json = await response.json();
                console.log('Успех:', JSON.stringify(json));
            } catch (error) {
                console.error('Ошибка:', error);
            }
        },*/
        getType(val) {
            let str = val.split('.')
            return str.pop()
        },
        closeModal() {
            document.getElementById('modal').style.display = 'none';
            this.type_error = ''
            this.title_error = ''
        },
        getFile(val, type) {
            this.new_item.file = val;
            this.new_file_type = type;
        },
        addElem() {
            if (this.new_item.date_start) {
                this.new_item.date_start = this.getDate(this.new_item.date_start)
            }
            if (this.new_item.type && this.new_item.title) {
                this.new_items.push(this.new_item);
                this.closeModal();
                this.new_item = {
                    type: null,
                    title: null,
                    number: null,
                    date_start: null,
                    date_end: null,
                    file: null
                }
                this.key_file = new Date().getTime();
            } else {
                if (!this.new_item.type) {
                    this.type_error = 'Выберите один вариант'
                }
                if (!this.new_item.title) {
                    this.title_error = 'Заполните поле'
                }
            }
        },
        getDate(val) {
            let new_date = new Date(val)
            return new_date.getDate() + '.' + new_date.getMonth() + '.' + new_date.getFullYear()
        }
    }
}
</script>

<style scoped lang="scss">
.documents {
    display   : flex;
    flex-wrap : wrap;

    &_item {
        display          : flex;
        padding          : 20px;
        border-radius    : 10px;
        margin-top       : 30px;
        background-color : #ffffff;
        text-decoration  : none;
        width            : calc(25% - 22.5px);
        margin-right     : 30px;
        align-items      : center;
        justify-content  : space-between;

        &:nth-child(4n) {
            margin-right : 0;
        }

        .item {
            &_title {
                font-weight : 700;
                font-size   : 24px;
                line-height : 29px;
                color       : #0d2839;
            }

            &_date {
                font-weight   : 400;
                font-size     : 18px;
                line-height   : 22px;
                color         : #86939C;
                margin-bottom : 18px;
            }

            &_status {
                height       : 22px;
                color        : #0d2839;
                font-size    : 18px;
                line-height  : 22px;
                padding-left : 18px;
                position     : relative;

                &:after {
                    content          : "";
                    position         : absolute;
                    left             : 0;
                    top              : 50%;
                    transform        : translateY(-50%);
                    border-radius    : 2px;
                    width            : 9px;
                    height           : 9px;
                    background-color : #9ecb45;
                }
            }

            &_icons {
                svg {
                    margin-right : 30px;
                }
            }
        }

        &_right {
            background-color : #f2f5f8;
            padding          : 30px;
            display          : flex;
            align-items      : center;
            justify-content  : center;
            border-radius    : 10px;
        }
    }

    @media (max-width : 1800px) {
        &_item {
            width : calc(33.3333% - 22.5px);

            &:nth-child(4n) {
                margin-right : 30px;
            }

            &:nth-child(3n) {
                margin-right : 0;
            }
        }
    }

    @media (max-width : 1300px) {
        &_item {
            width : calc(50% - 15px);

            &:nth-child(3n) {
                margin-right : 30px;
            }

            &:nth-child(2n) {
                margin-right : 0;
            }
        }
    }
}

#modal {
    display         : none;
    position        : fixed;
    overflow-y      : scroll;
    top             : 0;
    width           : 100vw;
    left            : 0;
    height          : 100vh;
    justify-content : center;
    padding         : 50px;
    background      : #0D283980;
    z-index         : 2;

    .backdrop {
        position : absolute;
        width    : 100%;
        height   : 100%;
        top      : 0;
        left     : 0;
        z-index  : 1;
    }

    .modal {
        width            : 650px;
        height           : fit-content;
        z-index          : 2;
        background-color : #ffffff;
        padding          : 30px;

        &_header {
            display         : flex;
            align-items     : center;
            justify-content : space-between;
            margin-bottom   : 50px;

            svg {
                cursor : pointer;
            }
        }

        &_title {
            color       : #458afb;
            font-weight : 700;
            font-size   : 36px;
            line-height : 43px;
        }

        &_type {
            display     : flex;
            align-items : flex-start;

            .left {
                span {
                    color : #fe6845;
                }
            }

            &_inputs {
                display        : flex;
                flex-direction : column;
                margin-left    : 17px;

                label {
                    margin-bottom : 10px;
                    font-size     : 18px;
                    line-height   : 22px;
                    color         : #0d2839;
                }
            }
        }

        .document {
            &_input {
                width         : 100%;
                border        : 0;
                border-bottom : 1px solid #b9c2c9;
                padding       : 12px 0;
                outline       : 0;
                color         : #86939c;
                font-size     : 18px;
                line-height   : 22px;
                margin-top    : 50px;
            }

            &_date {
                display     : flex;
                align-items : center;
                margin      : 0 50px;

                &_item {
                    display      : flex;
                    align-items  : center;
                    color        : #0d2839;
                    font-size    : 18px;
                    line-height  : 22px;
                    margin-right : 30px;

                    .dp__main {
                        width       : 157px;
                        margin-left : 15px;
                    }
                }
            }

            &_checkbox {
                font-weight   : 400;
                font-size     : 18px;
                line-height   : 22px;
                color         : #0D2839;
                margin-bottom : 20px;

                label {
                    position     : relative;
                    cursor       : pointer;
                    padding-left : 30px;

                    &:after {
                        position        : absolute;
                        content         : "";
                        left            : 0;
                        top             : 50%;
                        transform       : translateY(-50%);
                        width           : 20px;
                        height          : 20px;
                        border          : 1px solid #b9c2c9;
                        display         : flex;
                        align-items     : center;
                        justify-content : center;
                        padding         : 2px 0 0 1px;
                    }
                }

                &.active {
                    label:after {
                        background-color : #458afb;
                        border-color     : #458afb;
                        content          : url('/src/assets/check.svg');
                    }
                }
            }
        }

        &-footer {
            display         : flex;
            align-items     : center;
            justify-content : center;

            .add-elem {
                font-weight      : 800;
                font-size        : 16px;
                line-height      : 19px;
                text-transform   : uppercase;
                background-color : #ffbd27;
                color            : #ffffff;
                border-radius    : 10px;
                cursor           : pointer;
                width            : 220px;
                height           : 50px;
                display          : flex;
                align-items      : center;
                justify-content  : center;
            }

            .close_modal {
                font-size        : 16px;
                line-height      : 19px;
                font-weight      : 800;
                color            : #ffffff;
                text-transform   : uppercase;
                background-color : #d5dadf;
                width            : 220px;
                height           : 50px;
                margin-left      : 30px;
                display          : flex;
                align-items      : center;
                justify-content  : center;
                border-radius    : 10px;
                cursor           : pointer;
            }
        }
    }

    .error {
        color : #fe6845;
    }
}
</style>