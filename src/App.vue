<template>
  <ion-app>
    <ion-router-outlet ref="presentingElement" />
    <ion-modal
      ref="modal"
      :is-open="true"
      :presenting-element="presentingElement.$el"
      can-dismiss
      @didDismiss="emit('dismiss', false)"
    >
      <ion-nav
        id="order-modal-nav"
        ref="navRef"
        :root="OrderModalHome"
      />
    </ion-modal>
  </ion-app>
</template>

<script setup lang="ts">
import { IonApp, IonRouterOutlet, IonModal, IonNav } from '@ionic/vue';
</script>
