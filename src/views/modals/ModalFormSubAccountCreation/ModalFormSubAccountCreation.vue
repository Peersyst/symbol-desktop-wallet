<template>
    <div class="container">
        <Modal v-model="show" class-name="modal-container" :title="$t('modal_title_enter_account_name')" :transfer="false">
            <FormSubAccountCreation @submit="onSubmit" />
            <div slot="footer" class="modal-footer">
                <button type="submit" class="centered-button button-style back-button float-right" @click="show = false">
                    {{ $t('close') }}
                </button>
            </div>
        </Modal>
    </div>
</template>

<script lang="ts">
import { ModalFormSubAccountCreationTs } from './ModalFormSubAccountCreationTs';
export default class ModalFormSubAccountCreation extends ModalFormSubAccountCreationTs {}
</script>

<style lang="less" scoped>
.float-right {
    float: right;
}
</style>
