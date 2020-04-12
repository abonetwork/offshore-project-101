<template>
<div class="q-pa-md">
    <q-card class="my-card">
      <q-card-section>
        <div class="text-h6">1. Project Information</div>
        <q-separator />
        <br>
        <div class="row items-end">
          <div class="q-pa-xs col-4 col-md-2">
            <div class="col-sm-9 col-12 text-subtitle1">Company</div>
            <q-input outlined v-model="text" :dense="dense" label=""/>
          </div>
          <div class="q-pa-xs col-4 col-md-2">
            <div class="col-sm-9 col-12 text-subtitle1">Business Unit</div>
            <q-input outlined v-model="text" :dense="dense" label=""/>
          </div>
          <div class="q-pa-xs col-4 col-md-1">
            <div class="col-sm-9 col-12 text-subtitle1">Department</div>
            <q-input outlined v-model="text" :dense="dense" label="" />
          </div>
          <div class="q-pa-xs col-4 col-md-2">
            <div class="col-sm-9 col-12 text-subtitle1">PJ Account Mgr.</div>
            <q-input outlined v-model="text" :dense="dense" label="" />
          </div>
          <div class="q-pa-xs col-4 col-md-2">
            <div class="col-sm-9 col-12 text-subtitle1">Person who fills out a form</div>
            <q-input outlined v-model="text" :dense="dense" label="" />
          </div>
          <div class="q-pa-xs col-4 col-md-1">
            <div class="col-sm-9 col-12 text-subtitle1">Coins</div>
            <q-input outlined v-model="text" :dense="dense" label="" />
          </div>
          <div class="q-pa-xs col-4 col-md-2">
            <div class="col-sm-9 col-12 text-subtitle1">Email</div>
            <q-input outlined v-model="text" :dense="dense" label="" />
          </div>
        </div>
        <div class="row items-end">
          <div class="q-pa-xs col-4 col-md-1">
            <div class="col-sm-9 col-12 text-subtitle1">Phase</div>
            <q-select outlined v-model="modelPhase" :options="optionsPhase" :dense="dense" label="" />
          </div>
          <div class="q-pa-xs col-4 col-sm-2">
            <div class="col-sm-9 col-12 text-subtitle1">Date</div>
            <q-input outlined v-model="date" type="date" :dense="dense" >
            </q-input>
          </div>
          <div class="q-pa-xs col-4 col-md-1">
            <div class="col-sm-9 col-12 text-subtitle1">Go-live (plan)</div>
            <q-input outlined v-model="text" :dense="dense" label="" />
          </div>
          <div class="q-pa-xs col-4 col-md-1">
            <div class="col-sm-9 col-12 text-subtitle1">Go-live (actual)</div>
            <q-input outlined v-model="text" :dense="dense" label="" />
          </div>
          <div class="q-pa-xs col-4 col-md-1">
            <div class="col-sm-9 col-12 text-subtitle1">Phase start</div>
            <q-select outlined v-model="modelPhaseStart" :options="optionsPhase" :dense="dense" label="" />
          </div>
          <div class="q-pa-xs col-4 col-md-1">
            <div class="col-sm-9 col-12 text-subtitle1">Phase finish</div>
            <q-select outlined v-model="modelPhaseFin" :options="optionsPhase" :dense="dense" label="" />
          </div>
          <div class="q-pa-xs col-4 col-md-2">
            <div class="col-sm-9 col-12 text-subtitle1">Dev. type-detail</div>
            <q-input outlined v-model="text" :dense="dense" label="" />
          </div>
          <div class="q-pa-xs col-4 col-md-1">
            <div class="col-sm-9 col-12 text-subtitle1">Modification</div>
            <q-input outlined v-model="text" :dense="dense" label="" />
          </div>
          <div class="q-pa-xs col-4 col-md-2">
            <div class="col-sm-9 col-12 text-subtitle1">Social System Type</div>
            <q-input outlined v-model="text" :dense="dense" label="" />
          </div>
        </div>
        <br>
        <div class="row items-end">
          <div class="q-pa-xs col-4 col-md-4">
            <div class="col-sm-9 col-12 text-subtitle1">Project name</div>
            <q-input outlined v-model="text" :dense="dense" label="" />
          </div>
          <div class="q-pa-xs col-4 col-md-1">
            <div class="col-sm-9 col-12 text-subtitle1">Character</div>
            <q-input outlined v-model="text" :dense="dense" label="" />
          </div>
          <div class="q-pa-xs col-4 col-md-1">
            <div class="col-sm-9 col-12 text-subtitle1">System style</div>
            <q-input outlined v-model="text" :dense="dense" label="" />
          </div>
          <div class="q-pa-xs col-4 col-md-2">
            <div class="col-sm-9 col-12 text-subtitle1">Dev. type</div>
            <q-input outlined v-model="text" :dense="dense" label="" />
          </div>
          <div class="q-pa-xs col-4 col-md-2">
            <div class="col-sm-9 col-12 text-subtitle1">Customer name</div>
            <q-input outlined v-model="text" :dense="dense" label="" />
          </div>
          <div class="q-pa-xs col-4 col-md-2">
            <div class="col-sm-9 col-12 text-subtitle1">Customer category</div>
            <q-input outlined v-model="text" :dense="dense" label="" />
          </div>
        </div>
        <div class="row items-end">
          <div class="q-pa-xs col-4 col-md-4">
            <div class="col-sm-9 col-12 text-subtitle1">Industry</div><q-input outlined v-model="text" :dense="dense" label="" />
          </div>
          <div class="q-pa-xs col-4 col-md-3">
            <div class="col-sm-9 col-12 text-subtitle1">Business segment</div><q-input outlined v-model="text" :dense="dense" label="" />
          </div>
          <div class="q-pa-xs col-4 col-md-3">
            <div class="col-sm-9 col-12 text-subtitle1">Business name</div><q-input outlined v-model="text" :dense="dense" label="" />
          </div>
          <div class="q-pa-xs col-4 col-md-2">
            <div class="col-sm-9 col-12 text-subtitle1">Project #</div><q-input outlined v-model="text" :dense="dense" label="" />
          </div>
        </div>
        <div class="row items-end">
          <div class="q-pa-xs col-4 col-md-2">
            <div class="col-sm-9 col-12 text-subtitle1">Dev. language(1)</div><q-input outlined v-model="text" :dense="dense" label="" />
          </div>
          <div class="q-pa-xs col-4 col-md-2">
            <div class="col-sm-9 col-12 text-subtitle1">Dev. language(2)</div><q-input outlined v-model="text" :dense="dense" label="" />
          </div>
          <div class="q-pa-xs col-4 col-md-2">
            <div class="col-sm-9 col-12 text-subtitle1">Dev. language(3)</div><q-input outlined v-model="text" :dense="dense" label="" />
          </div>
          <div class="q-pa-xs col-4 col-md-1">
            <div class="col-sm-9 col-12 text-subtitle1">Main OS</div><q-input outlined v-model="text" :dense="dense" label="" />
          </div>
          <div class="q-pa-xs col-4 col-md-1">
            <div class="col-sm-9 col-12 text-subtitle1">DBMS</div><q-input outlined v-model="text" :dense="dense" label="" />
          </div>
          <div class="q-pa-xs col-4 col-md-2">
            <div class="col-sm-9 col-12 text-subtitle1">Framework</div><q-input outlined v-model="text" :dense="dense" label="" />
          </div>
        </div>
        <div class="row items-end">
          <div class="q-pa-xs col-12 col-md-12" >
            <div class="col-sm-9 col-12 text-subtitle1">PJ overview & character</div>
            <q-input v-model="text" outlined :dense="dense" type="textarea"  label=""/>
          </div>
        </div>
      </q-card-section>
    </q-card>
  </div>
</template>

<script>
export default {
  name: 'PageIndex',
  data () {
    return {
      text: '',
      modelPhase: null,
      modelPhaseStart: null,
      modelPhaseFin: null,
      optionsPhase: ['RD', 'UI', 'SS', 'PS', 'PG', 'PT', 'IT', 'ST', 'OT', 'OM'],
      date: '',
      dense: true
    }
  }

}
</script>

<style lang="sass" scoped>
.my-card
  width: 100%
  // max-width: 1200px
</style>
