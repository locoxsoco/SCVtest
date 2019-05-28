<template>
  <div class="content">
    <div class="container-fluid">
      <div class="row">
        <div class="col-12">
          <card class="strpied-tabled-with-hover"
                body-classes="table-full-width table-responsive"
          >
            <template slot="header">
              <h4 class="card-title">Aeropuerto Jorge Chavez</h4>
              <p class="card-category">Llegadas</p>
            </template>
            <l-table class="table-hover table-striped"
                     :columns="table1.columns"
                     :data="table1.data"
                     style="margin-left:0px !important">
            </l-table>
          </card>

        </div>

        <!--<div class="col-12">
          <card class="card-plain">
            <template slot="header">
              <h4 class="card-title">Table on Plain Background</h4>
              <p class="card-category">Here is a subtitle for this table</p>
            </template>
            <div class="table-responsive">
              <l-table class="table-hover"
                       :columns="table2.columns"
                       :data="table2.data">
              </l-table>
            </div>
          </card>
        </div>

        <div class="col-12">
          <card class="strpied-tabled-with-hover"
                body-classes="table-full-width table-responsive"
          >
            <template slot="header">
              <h4 class="card-title">Small table</h4>
              <p class="card-category">Here is a subtitle for this table</p>
            </template>
            <l-table class="table-hover table-striped table-sm"
                     :columns="table1.columns"
                     :data="table1.data">
            </l-table>
          </card>

        </div>-->

      </div>
    </div>
  </div>
</template>
<script>
  import LTable from 'src/components/Table.vue'
  import Card from 'src/components/Cards/Card.vue'
  const tableColumns = ['Aerolinea', 'Vuelo', 'Procedencia', 'HoraProgramada', 'HoraReal','Estado','Puerta']
  const tableData = [{
    aerolinea: 1,
    vuelo: 'Dakota Rice',
    procedencia: '$36.738',
    horaprogramada: 'Niger',
    horareal: 'Oud-Turnhout',
    estado: 'En vuelo',
    puerta: 50
  },
  {
    aerolinea: 2,
    vuelo: 'Minerva Hooper',
    procedencia: '$23,789',
    horaprogramada: 'Curaçao',
    horareal: 'Sinaai-Waas',
    estado: 'En vuelo',
    puerta: 28
  },
  {
    aerolinea: 3,
    vuelo: 'Sage Rodriguez',
    procedencia: '$56,142',
    horaprogramada: 'Netherlands',
    horareal: 'Baileux',
    estado: 'En vuelo',
    puerta: 43
  },
  {
    aerolinea: 4,
    vuelo: 'Philip Chaney',
    procedencia: '$38,735',
    horaprogramada: 'Korea, South',
    horareal: 'Overland Park',
    estado: 'En vuelo',
    puerta: 18
  },
  {
    aerolinea: 5,
    vuelo: 'Doris Greene',
    procedencia: '$63,542',
    horaprogramada: 'Malawi',
    horareal: 'Feldkirchen in Kärnten',
    estado: 'En vuelo',
    puerta: 6
  }]
  export default {
    components: {
      LTable,
      Card
    },
    data () {
      return {
        table1: {
          columns: [...tableColumns],
          data: [...tableData]
        },
        table2: {
          columns: [...tableColumns],
          data: [...tableData]
        }
      }
    }
  }
</script>
<style>
</style>
