<template>

    <div>
        <div class="sidebar-wrapper bg-white">
            <div class="logo-wrapper text-center py-25 px-10">
                <img class="big-image" :src="static_image['dashboard_logo']" alt="gplex">
                <img class="small-image" :src="static_image['dashboard_sm_logo']" height="50" alt="gplex">
            </div>
            <nav class="sidebar-menu-wrapper text-left">
                <ul class="main-items mb-0 pl-10 py-30 list-unstyled">
                    <li>
                        <router-link :to="{ name: 'dashboard'}">
               <span class="anim">
                  <span class="anim">
                     <svg version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" viewBox="0 0 17.5 20" style="enable-background:new 0 0 17.5 20;" xml:space="preserve">
                        <g>
                           <path id="Icon_material-dashboard_1_" class="st0" d="M1.3,10.8h6.6V2.6H1.3V10.8z M1.3,17.4h6.6v-5H1.3V17.4z M9.6,17.4h6.6V9.2
                              H9.6V17.4z M9.6,2.6v5h6.6v-5H9.6z"/>
                        </g>
                     </svg>
                  </span>
               </span>
                            <span class="menu-title">
               Dashboard
               </span>
                        </router-link>
                    </li>

                    <li  v-if="checkPermission('category-list')">
                        <router-link :to="{ name: 'categoryList'}">
               <span class="anim">
                  <svg version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" viewBox="0 0 17.5 20" style="enable-background:new 0 0 17.5 20;" xml:space="preserve">
                     <g>
                        <path id="Icon_awesome-share-alt_1_" class="st0" d="M13,12.1c-0.7,0-1.4,0.2-2,0.7l-3.4-2.1c0.1-0.5,0.1-0.9,0-1.4L11,7.2
                           c1.4,1.1,3.4,0.9,4.5-0.5s0.9-3.4-0.5-4.5s-3.4-0.9-4.5,0.5C9.9,3.5,9.7,4.4,9.9,5.4L6.5,7.5C5.1,6.4,3.1,6.6,2,8s-0.9,3.4,0.5,4.5
                           c1.2,0.9,2.8,0.9,4,0l3.4,2.1c-0.4,1.7,0.7,3.4,2.4,3.8c1.7,0.4,3.4-0.7,3.8-2.4c0.4-1.7-0.7-3.4-2.4-3.8
                           C13.5,12.1,13.2,12.1,13,12.1z"/>
                     </g>
                  </svg>
               </span>
                            <span class="menu-title">Category</span>
                        </router-link>
                    </li>
                    <li  v-if="checkPermission('article-list')">
                        <router-link :to="{ name: 'articleList'}">
               <span class="anim">
                  <svg version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" viewBox="0 0 17.5 20" style="enable-background:new 0 0 17.5 20;" xml:space="preserve">
                     <g>
                        <path id="Icon_ionic-ios-help-buoy_1_" class="st0" d="M8.8,2C4.4,2,0.9,5.6,0.9,10s3.6,7.9,7.9,7.9s7.9-3.6,7.9-7.9
                           C16.7,5.6,13.2,2,8.8,2C8.8,2,8.8,2,8.8,2z M10.9,3.4c2.1,0.7,3.8,2.3,4.5,4.5L12,8.1c-0.3-0.5-0.8-1-1.3-1.3L10.9,3.4z M3.9,5.1
                           c0.8-0.8,1.7-1.4,2.8-1.7l0.2,3.4C6.4,7.1,6,7.6,5.6,8.1L2.2,7.9C2.6,6.8,3.2,5.9,3.9,5.1z M6.7,16.5c-2.1-0.7-3.8-2.3-4.5-4.5
                           l3.4-0.2c0.3,0.5,0.8,1,1.3,1.3L6.7,16.5z M8.8,12.6c-1.4,0-2.6-1.2-2.6-2.6s1.2-2.6,2.6-2.6s2.6,1.2,2.6,2.6
                           C11.4,11.4,10.2,12.6,8.8,12.6z M13.7,14.8c-0.8,0.8-1.7,1.4-2.8,1.7l-0.2-3.4c0.5-0.3,1-0.8,1.3-1.3l3.4,0.2
                           C15,13.1,14.4,14,13.7,14.8L13.7,14.8z"/>
                     </g>
                  </svg>
               </span>
                            <span class="menu-title">Article</span>
                        </router-link>
                    </li>
                    <li v-if="checkPermission('faq-list')">
                        <router-link :to="{ name: 'faqList'}">
               <span class="anim">
                  <svg version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" viewBox="0 0 17.5 20" style="enable-background:new 0 0 17.5 20;" xml:space="preserve">
                     <g>
                        <g>
                           <path id="Path_112_1_" class="st0" d="M14.9,7.4H7.3C6.6,7.4,6,8,6,8.7V14c0,0.7,0.6,1.3,1.3,1.3h4.3c0.1,0,0.2,0,0.3,0.1l2.2,2
                              c0.1,0.1,0.3,0.1,0.3-0.1v-1.7c0-0.2,0.1-0.3,0.3-0.3h0c0.7,0,1.4-0.6,1.4-1.3V8.7C16.2,8,15.6,7.4,14.9,7.4
                              C14.9,7.4,14.9,7.4,14.9,7.4z"/>
                        </g>
                        <g>
                           <path id="Path_113_1_" class="st0" d="M5.6,5.9h6.1V3.7c0-0.6-0.5-1.1-1.1-1.1H2.4C1.8,2.5,1.3,3,1.3,3.7v5.6
                              c0,0.6,0.5,1.1,1.1,1.1h2.1V7C4.5,6.4,5,5.9,5.6,5.9z"/>
                        </g>
                     </g>
                  </svg>
               </span>
                            <span class="menu-title">FAQ</span>
                        </router-link>
                    </li>

                    <li v-if="checkPermission('quiz-list') || checkPermission('quiz-form-list') || checkPermission('quiz-form-field-list')">
                        <a href="#pageSubmenu" data-toggle="collapse" aria-expanded="false" class="dropdown-toggle collapsed">
                   <span class="anim">
                      <svg version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" viewBox="0 0 17.5 20" style="enable-background:new 0 0 17.5 20;" xml:space="preserve">
                         <g>
                            <path id="Icon_awesome-skiing_1_" class="st0" d="M13.8,5.4c0.8,0,1.4-0.6,1.4-1.4s-0.6-1.4-1.4-1.4c-0.8,0-1.4,0.6-1.4,1.4
                               S13,5.4,13.8,5.4z M15.9,15.6c-0.3-0.3-0.7-0.3-1,0c0,0,0,0,0,0c-0.3,0.3-0.9,0.4-1.3,0.3l-3.9-2l1.4-2.1c0.4-0.5,0.3-1.3-0.2-1.7
                               L9.8,8.8L6.7,7.3C6.6,7.9,6.8,8.5,7.2,8.9L9.4,11l-1.3,2l-5.7-2.9c-0.3-0.2-0.8,0-0.9,0.3c-0.2,0.3,0,0.8,0.3,0.9l0,0L13,17.1
                               c0.3,0.2,0.7,0.2,1.1,0.2c0.7,0,1.3-0.3,1.8-0.7C16.2,16.3,16.2,15.9,15.9,15.6C15.9,15.6,15.9,15.6,15.9,15.6z M4.8,5.3L4.5,5.9
                               c0.4,0.2,0.9,0.1,1.2-0.1l1.4,0.7c0,0,0,0,0,0l3.3,1.6l0.9-0.4l0.2,0.5c0.1,0.3,0.4,0.6,0.7,0.8l1.7,0.8c0.5,0.2,1,0,1.2-0.4
                               c0.2-0.4,0-1-0.4-1.2l-1.5-0.8L12.7,6c-0.3-1-1.4-1.5-2.3-1.2c0,0-0.1,0-0.1,0L7.9,5.8L6.1,4.9c0-0.4-0.2-0.8-0.6-1L5.2,4.6h0
                               l-1-0.2c-0.1,0-0.1,0-0.1,0C4,4.5,4,4.5,4.1,4.6c0,0,0,0,0,0L4.8,5.3z"/>
                         </g>
                      </svg>
                   </span>
                            <span class="menu-title">Quiz</span>
                        </a>
                        <ul class="collapse list-unstyled sub-items" id="pageSubmenu">
                            <li v-if="checkPermission('quiz-form-list')">
                                <router-link :to="{ name: 'quizFormList'}">
                                    <span class="menu-sub-title">Quiz Forms</span>
                                </router-link>
                            </li>
                            <li  v-if="checkPermission('quiz-form-field-list')">
                                <router-link :to="{ name: 'quizFormFieldList'}">
                                    <span class="menu-sub-title">Quiz Form Field</span>
                                </router-link>
                            </li>
                            <li v-if="checkPermission('quiz-list')">
                                <router-link :to="{ name: 'quizList'}">
                                    <span class="menu-sub-title">Quizzes</span>
                                </router-link>
                            </li>
                        </ul>
                    </li>


                    <li v-if="checkPermission('notification-list') || checkPermission('history-list') || checkPermission('result-list')">
                        <a href="#reportSubmenu" data-toggle="collapse" aria-expanded="false" class="dropdown-toggle collapsed">
               <span class="anim">
                  <svg version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" viewBox="0 0 17.5 20" style="enable-background:new 0 0 17.5 20;" xml:space="preserve">
                     <g>
                        <path id="Icon_ionic-ios-settings_1_" class="st0" d="M15,10c0-0.8,0.5-1.5,1.2-1.8c-0.2-0.8-0.5-1.5-0.9-2.2
                           c-0.2,0.1-0.5,0.2-0.8,0.2c-1.1,0-1.9-0.9-1.9-1.9c0-0.3,0.1-0.5,0.2-0.8c-0.7-0.4-1.4-0.7-2.2-0.9c-0.4,1-1.5,1.5-2.5,1.1
                           C7.5,3.4,7.1,3,7,2.5C6.2,2.7,5.4,3,4.7,3.4c0.4,1,0,2.1-1,2.5C3.5,6.1,3.2,6.1,3,6.1C2.7,6.1,2.4,6.1,2.2,6
                           C1.8,6.7,1.4,7.4,1.3,8.2c1,0.4,1.5,1.5,1.1,2.5c-0.2,0.5-0.6,0.9-1.1,1.1c0.2,0.8,0.5,1.5,0.9,2.2c1-0.4,2.1,0,2.5,1
                           c0.2,0.5,0.2,1.1,0,1.6c0.7,0.4,1.4,0.7,2.2,0.9c0.4-1,1.5-1.5,2.5-1.1c0.5,0.2,0.9,0.6,1.1,1.1c0.8-0.2,1.5-0.5,2.2-0.9
                           c-0.4-1,0-2.1,1-2.5c0.5-0.2,1.1-0.2,1.6,0c0.4-0.7,0.7-1.4,0.9-2.2C15.5,11.5,15,10.8,15,10z M8.8,13.1c-1.7,0-3.1-1.4-3.1-3.1
                           s1.4-3.1,3.1-3.1s3.1,1.4,3.1,3.1c0,0,0,0,0,0C11.9,11.7,10.5,13.1,8.8,13.1z"/>
                     </g>
                  </svg>
               </span>
                            <span class="menu-title">Reports</span>
                        </a>
                        <ul class="collapse list-unstyled sub-items" id="reportSubmenu">
                            <li v-if="checkPermission('notification-list')">
                                <router-link :to="{ name: 'notificationList'}">
                                    <span class="menu-sub-title">Notifications</span>
                                </router-link>
                            </li>

                            <li v-if="checkPermission('history-list')">
                                <router-link :to="{ name: 'allHistoryList'}">
                                    <span class="menu-sub-title">Histories</span>
                                </router-link>
                            </li>

                            <li v-if="checkPermission('result-list')">
                                <router-link :to="{ name: 'resultList'}">
                                    <span class="menu-sub-title">Results</span>
                                </router-link>
                            </li>
                            <li v-if="checkPermission('result-list')">
                                <router-link :to="{ name: 'quizResultList'}">
                                    <span class="menu-sub-title">Quiz Results</span>
                                </router-link>
                            </li>
                        </ul>
                    </li>


                    <li
                            v-if="checkPermission('user-list') ||
                          checkPermission('role-list') ||
                          checkPermission('banner-list') ||
                          checkPermission('comment-list') ||
                          checkPermission('page-create') ||
                          checkPermission('email-create')"
                    >
                        <a href="#settingSubmenu" data-toggle="collapse" aria-expanded="false" class="dropdown-toggle collapsed">
               <span class="anim">
                  <svg version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" viewBox="0 0 17.5 20" style="enable-background:new 0 0 17.5 20;" xml:space="preserve">
                     <g>
                        <path id="Icon_ionic-ios-settings_1_" class="st0" d="M15,10c0-0.8,0.5-1.5,1.2-1.8c-0.2-0.8-0.5-1.5-0.9-2.2
                           c-0.2,0.1-0.5,0.2-0.8,0.2c-1.1,0-1.9-0.9-1.9-1.9c0-0.3,0.1-0.5,0.2-0.8c-0.7-0.4-1.4-0.7-2.2-0.9c-0.4,1-1.5,1.5-2.5,1.1
                           C7.5,3.4,7.1,3,7,2.5C6.2,2.7,5.4,3,4.7,3.4c0.4,1,0,2.1-1,2.5C3.5,6.1,3.2,6.1,3,6.1C2.7,6.1,2.4,6.1,2.2,6
                           C1.8,6.7,1.4,7.4,1.3,8.2c1,0.4,1.5,1.5,1.1,2.5c-0.2,0.5-0.6,0.9-1.1,1.1c0.2,0.8,0.5,1.5,0.9,2.2c1-0.4,2.1,0,2.5,1
                           c0.2,0.5,0.2,1.1,0,1.6c0.7,0.4,1.4,0.7,2.2,0.9c0.4-1,1.5-1.5,2.5-1.1c0.5,0.2,0.9,0.6,1.1,1.1c0.8-0.2,1.5-0.5,2.2-0.9
                           c-0.4-1,0-2.1,1-2.5c0.5-0.2,1.1-0.2,1.6,0c0.4-0.7,0.7-1.4,0.9-2.2C15.5,11.5,15,10.8,15,10z M8.8,13.1c-1.7,0-3.1-1.4-3.1-3.1
                           s1.4-3.1,3.1-3.1s3.1,1.4,3.1,3.1c0,0,0,0,0,0C11.9,11.7,10.5,13.1,8.8,13.1z"/>
                     </g>
                  </svg>
               </span>
                            <span class="menu-title">Settings</span>
                        </a>
                        <ul class="collapse list-unstyled sub-items" id="settingSubmenu">
                            <!-- <li v-if="checkPermission('group-list')">
                                <router-link :to="{ name: 'groupList'}">
                                    <span class="menu-sub-title">Groups</span>
                                </router-link>
                            </li> -->

                            <li v-if="checkPermission('menu-list')">
                                
                                <router-link :to="{ name: 'menuList'}">
                                    <span class="menu-sub-title">Menus</span>
                                </router-link>
                            </li>

                            <li v-if="checkPermission('page-list')">
                                
                                <router-link :to="{ name: 'pageList'}">
                                    <span class="menu-sub-title">Pages</span>
                                </router-link>
                            </li>


                            <!-- <li v-if="checkPermission('menu-list')">
                                <router-link :to="{ name: 'roleList'}">
                                    <span class="menu-sub-title">Pages</span>
                                </router-link>
                            </li> -->

                            <li v-if="checkPermission('role-list')">
                                <router-link :to="{ name: 'roleList'}">
                                    <span class="menu-sub-title">Roles</span>
                                </router-link>
                            </li>


                            <li v-if="checkPermission('user-list')">
                                <router-link :to="{ name: 'customerList'}">
                                    <span class="menu-sub-title">Users</span>
                                </router-link>
                            </li>

                            <li v-if="checkPermission('banner-list')">
                                <router-link :to="{ name: 'bannerList'}">
                                    <span class="menu-sub-title">Banners</span>
                                </router-link>
                            </li>
                            <li v-if="checkPermission('comment-list')">
                                <router-link :to="{ name: 'commentList'}">
                                    <span class="menu-sub-title">Comments</span>
                                </router-link>
                            </li>
                            <li v-if="checkPermission('email-create') && checkPermission('page-edit')">
                                <a href="#" @click="isEmailConfigurationCheck=true" class="ripple-btn right-side-config-form">
                                    <span class="menu-sub-title">Email Configuration</span>
                                </a>
                            </li>
                            <li v-if="checkPermission('page-create') && checkPermission('page-edit')">
                                <a href="#" @click="isConfigurationCheck=true" class="ripple-btn right-side-config-form">
                                    <span class="menu-sub-title">Front Page Configuration</span>
                                </a>
                            </li>


                                <!-- v-if="checkPermission('link-list')" -->
                            <li >   
                                <router-link :to="{ name: 'linkList'}">
                                    <span class="menu-sub-title">Useful Links</span>
                                </router-link>
                            </li>

                            <li >   
                                <router-link :to="{ name: 'interestRate'}">
                                    <span class="menu-sub-title">Interest Rate</span>
                                </router-link>
                            </li>

                            <li >   
                                <router-link :to="{ name: 'exchangeRate'}">
                                    <span class="menu-sub-title">Exchange Rate</span>
                                </router-link>
                            </li>

                        </ul>
                    </li>
                </ul>
            </nav>
        </div>
        <div class="right-sidebar-wrapper right-side-config-wrapper with-upper-shape fixed-top px-20 pb-30 pb-md-40 pt-70" >
            <div class="close-bar d-flex align-items-center justify-content-end">
                <button class="right-side-config-close-btn ripple-btn-danger" @click="clearAllChecker">
                    <img src="../../assets/img/cancel.svg" alt="cancel">
                </button>
            </div>
            <pageConfiguration v-if="isConfigurationCheck" :isConfigurationCheck="isConfigurationCheck" @page-config-close="getDataFromChild"></pageConfiguration>
            <emailConfiguration v-if="isEmailConfigurationCheck" :isEmailConfigurationCheck="isEmailConfigurationCheck" @email-config-close="getDataFromChild"></emailConfiguration>
        </div>
        <div class="action-modal-wraper" v-if="success_message">
            <span>{{ success_message }}</span>
        </div>
        <div class="action-modal-wraper-error" v-if="error_message">
            <span>{{ error_message }}</span>
        </div>
    </div>



</template>

<script>
    import pageConfiguration from "@/components/settings/pageConfigurationNew";
    import emailConfiguration from "@/components/settings/emailConfiguration";
    import axios from "axios";
    import $ from "jquery";

    export default {
        name: "Menu.vue",

        components: {
            pageConfiguration,
            emailConfiguration
        },

        data() {
            return {
                isConfigurationCheck : false,
                isEmailConfigurationCheck : false,
                token            : '',
                user_permissions : '',
                mappedPermission : '',
                user_info        : '',
                success_message     : '',
                error_message       : '',
                static_image        : [],
            }
        },
        methods :{
            removingRightSideWrapper()
            {
                console.log('working')
                this.isConfigurationCheck = false;
                this.isEmailConfigurationCheck = false;

                document.body.classList.remove('open-side-slider');
                $('.right-sidebar-wrapper.right-side-config-wrapper').toggleClass('right-side-config-form-show');
            },
            getDataFromChild(status)
            {
                console.log(status);
                this.success_message = status;
                this.setTimeoutElements();
                this.removingRightSideWrapper();
            },
            setTimeoutElements()
            {
                setTimeout(() => this.success_message = "", 2e3);
                setTimeout(() => this.error_message = "", 2e3);
            },

            checkPermission(permissionForCheck){

                if ((this.mappedPermission).includes(permissionForCheck) === true) {
                    return true;
                } else {
                    return false;
                }

            },

            clearAllChecker()
            {
                this.isConfigurationCheck      = false;
                this.isEmailConfigurationCheck = false;
            },

            getPageConfigData(newData)
            {
                console.log(newData)
                this.isConfigurationCheck = false;
            },
        },
        created() {
            this.user_info          = JSON.parse(localStorage.getItem("userInformation"));
            this.user_permissions   = JSON.parse(localStorage.getItem("userPermissions"));
            this.mappedPermission   = (this.user_permissions ).map(x => x.slug);
            //console.log( localStorage.getItem("userPermissions"));
            this.static_image['dashboard_logo']     = axios.defaults.baseURL.replace('api/','')+'static_media/new-logo.png';
            this.static_image['dashboard_sm_logo'] = axios.defaults.baseURL.replace('api/','')+'static_media/small-logo.png';
        }
    }
</script>

<style scoped>

</style>
