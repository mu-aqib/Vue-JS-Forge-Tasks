<script setup lang="ts">
    import { Button as KButton } from '@progress/kendo-vue-buttons';
    import { Popup as KPopup } from '@progress/kendo-vue-popup';
    import { ref } from 'vue';

    const showTeamsPopup = ref(false)
</script>

<template>
    <nav>
        <div class="flex border-bottom border-2 p-4 justify-between">
            <AppImage src="https://vuejsforge.com/images/logo-vuejs-forge.svg" alt="logo-img" width="150" />
            
            <div>
                <button class="mr-4 text-[#ff6538]" ref="teamButton" @click="showTeamsPopup = !showTeamsPopup">
                    <span class="k-icon k-i-ungroup"></span>
                    My Team
                </button>
                <KPopup :anchor="'teamButton'" :show="showTeamsPopup" class="mt-5">
                    <ul>
                        <li class="px-5 py-2" @click="showTeamsPopup = false">Team 1</li>
                        <li class="px-5 py-2" @click="showTeamsPopup = false">Team 2</li>
                    </ul>
                </KPopup>

                <KButton :theme-color="'secondary'">Logout</KButton>
            </div>
        </div>
    </nav>
</template>

