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
            <q-input outlined v-model="modelcompany" :dense="dense" label=""/>
          </div>
          <div class="q-pa-xs col-4 col-md-2">
            <div class="col-sm-9 col-12 text-subtitle1">Business Unit</div>
            <q-input outlined v-model="modelbusinessUnit" :dense="dense" label=""/>
          </div>
          <div class="q-pa-xs col-4 col-md-1">
            <div class="col-sm-9 col-12 text-subtitle1">Department</div>
            <q-input outlined v-model="modeldepartment" :dense="dense" label="" />
          </div>
          <div class="q-pa-xs col-4 col-md-2">
            <div class="col-sm-9 col-12 text-subtitle1">PJ Account Mgr.</div>
            <q-input outlined v-model="modelprjAccountMgr" :dense="dense" label="" />
          </div>
          <div class="q-pa-xs col-4 col-md-2">
            <div class="col-sm-9 col-12 text-subtitle1">Person who fills out a form</div>
            <q-input outlined v-model="modelpersonWhoFill" :dense="dense" label="" />
          </div>
          <div class="q-pa-xs col-4 col-md-1">
            <div class="col-sm-9 col-12 text-subtitle1">Coins</div>
            <q-input outlined v-model="modelcoins" :dense="dense" label="" />
          </div>
          <div class="q-pa-xs col-4 col-md-2">
            <div class="col-sm-9 col-12 text-subtitle1">Email</div>
            <q-input outlined v-model="modelemail" :dense="dense" label="" />
          </div>
        </div>
        <div class="row items-end">
          <div class="q-pa-xs col-4 col-md-1">
            <div class="col-sm-9 col-12 text-subtitle1">Phase</div>
            <q-select outlined v-model="modelPhase" :options="optionsPhase" :dense="dense" label="" />
          </div>
          <div class="q-pa-xs col-4 col-sm-2">
            <div class="col-sm-9 col-12 text-subtitle1">Date</div>
            <q-input outlined v-model="modeldate" :dense="dense" mask="date" >
              <template v-slot:append>
                <q-icon name="event" class="cursor-pointer">
                  <q-popup-proxy ref="qDateProxy" transition-show="scale" transition-hide="scale">
                    <q-date v-model="modeldate" @input="() => $refs.qDateProxy.hide()" />
                  </q-popup-proxy>
                </q-icon>
              </template>
            </q-input>
          </div>
          <div class="q-pa-xs col-4 col-md-1">
            <div class="col-sm-9 col-12 text-subtitle1">Go-live (plan)</div>
            <q-input outlined v-model="modelgoLivePlan" :dense="dense" label="" />
          </div>
          <div class="q-pa-xs col-4 col-md-1">
            <div class="col-sm-9 col-12 text-subtitle1">Go-live (actual)</div>
            <q-input outlined v-model="modelgoLiveActual" :dense="dense" label="" />
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
            <q-input outlined v-model="modeldevTypeDetail" :dense="dense" label="" />
          </div>
          <div class="q-pa-xs col-4 col-md-1">
            <div class="col-sm-9 col-12 text-subtitle1">Modification</div>
            <q-input outlined v-model="modelmodification" :dense="dense" label="" />
          </div>
          <div class="q-pa-xs col-4 col-md-2">
            <div class="col-sm-9 col-12 text-subtitle1">Social System Type</div>
            <q-input outlined v-model="modelsocialSystemType" :dense="dense" label="" />
          </div>
        </div>
        <br>
        <div class="row items-end">
          <div class="q-pa-xs col-4 col-md-4">
            <div class="col-sm-9 col-12 text-subtitle1">Project name</div>
            <q-input outlined v-model="modelprojectName" :dense="dense" label="" />
          </div>
          <div class="q-pa-xs col-4 col-md-1">
            <div class="col-sm-9 col-12 text-subtitle1">Character</div>
            <q-input outlined v-model="modelcharacter" :dense="dense" label="" />
          </div>
          <div class="q-pa-xs col-4 col-md-1">
            <div class="col-sm-9 col-12 text-subtitle1">System style</div>
            <q-input outlined v-model="modelsystemStyle" :dense="dense" label="" />
          </div>
          <div class="q-pa-xs col-4 col-md-2">
            <div class="col-sm-9 col-12 text-subtitle1">Dev. type</div>
            <q-input outlined v-model="modeldevType" :dense="dense" label="" />
          </div>
          <div class="q-pa-xs col-4 col-md-2">
            <div class="col-sm-9 col-12 text-subtitle1">Customer name</div>
            <q-input outlined v-model="modelcustomerName" :dense="dense" label="" />
          </div>
          <div class="q-pa-xs col-4 col-md-2">
            <div class="col-sm-9 col-12 text-subtitle1">Customer category</div>
            <q-input outlined v-model="modelcustomerCategory" :dense="dense" label="" />
          </div>
        </div>
        <div class="row items-end">
          <div class="q-pa-xs col-4 col-md-4">
            <div class="col-sm-9 col-12 text-subtitle1">Industry</div>
            <q-input outlined v-model="modelindustry" :dense="dense" label="" />
          </div>
          <div class="q-pa-xs col-4 col-md-3">
            <div class="col-sm-9 col-12 text-subtitle1">Business segment</div>
            <q-input outlined v-model="modelbusinessSegment" :dense="dense" label="" />
          </div>
          <div class="q-pa-xs col-4 col-md-3">
            <div class="col-sm-9 col-12 text-subtitle1">Business name</div>
            <q-input outlined v-model="modelbusinessName" :dense="dense" label="" />
          </div>
          <div class="q-pa-xs col-4 col-md-2">
            <div class="col-sm-9 col-12 text-subtitle1">Project #</div>
            <q-input outlined v-model="modelprojectNo" :dense="dense" label="" />
          </div>
        </div>
        <div class="row items-end">
          <div class="q-pa-xs col-4 col-md-4">
            <div class="col-sm-9 col-12 text-subtitle1">Dev. language</div>
            <q-select outlined v-model="modelDevLang" multiple :options="optionsDevLang" :dense="dense" max-values="3" hide-hint="true"/>
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
            <q-input v-model="modelpjOverviewAndCharacter" outlined :dense="dense" type="textarea"  label=""/>
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
      modelcompany: '',
      modelbusinessUnit: '',
      modeldepartment: '',
      modelprjAccountMgr: '',
      modelpersonWhoFill: '',
      modelcoins: '',
      modelemail: '',
      modelPhase: null,
      modelgoLivePlan: '',
      modelgoLiveActual: '',
      modelPhaseStart: null,
      modelPhaseFin: null,
      modeldevTypeDetail: '',
      modelmodification: '',
      modelsocialSystemType: '',
      modelprojectName: '',
      modelcharacter: '',
      modelsystemStyle: '',
      modeldevType: '',
      modelcustomerName: '',
      modelcustomerCategory: '',
      modelindustry: '',
      modelbusinessSegment: '',
      modelbusinessName: '',
      modelprojectNo: '',
      modelDevLang: '',
      modelmainOS: '',
      modeldbms: '',
      modelframework: '',
      optionsPhase: ['RD', 'UI', 'SS', 'PS', 'PG', 'PT', 'IT', 'ST', 'OT', 'OM'],
      optionsDevLang: ['Assembler', 'COBOL', 'PL/I', 'Pro*C', 'C++', 'C', 'VB', 'Excel(VBA)', 'InputMan', 'PL/SQL', 'ABAP', 'C# ', 'Visual Basic .NET', 'Java', 'Perl', 'Shell Script', 'Delphi', 'HTML', 'XML', 'Ruby', 'PHP', 'Other languages'],
      modelpjOverviewAndCharacter: '',
      modeldate: '',
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
