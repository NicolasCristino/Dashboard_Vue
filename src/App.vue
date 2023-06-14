<template>
  <v-app theme="dark">
    <v-navigation-drawer v-model="isDrawerOpen">
      <v-list>
        <v-list-subheader>Menu</v-list-subheader>
        <v-list-item prepend-icon="mdi-home">Home</v-list-item>
        <v-list-item prepend-icon="mdi-account">Usuários</v-list-item>

        <v-list-group value="Clientes">
          <template v-slot:activator="{ props }">
            <v-list-item
              v-bind="props"
              prepend-icon="mdi-account-circle"
              title="Clientes"
            ></v-list-item>
          </template>

          <v-list-item prepend-icon="mdi-currency-usd">Faturamento</v-list-item>
          <v-list-item prepend-icon="mdi-note">Relatório</v-list-item>
          <v-list-item prepend-icon="mdi-send">Emissão</v-list-item>
        </v-list-group>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar flat class="border-b">
      <v-app-bar-nav-icon @click="isDrawerOpen = !isDrawerOpen"></v-app-bar-nav-icon>

      <template #append>
        <v-menu>
          <template #activator="{ props }">
            <v-btn icon class="mr-2" v-bind="props">
              <v-badge dot color="info">
                <v-icon icon="mdi-bell-outline"></v-icon>
              </v-badge>
            </v-btn>
          </template>

          <v-card width="400px">
              <v-list nav density="default" :lines="false"> 

                <v-list-item append-icon="mdi-message-outline">
                  <v-list-item-title class="text-h6 text-wrap mb-2">
                    Bom dia
                  </v-list-item-title>

                  <v-list-item-subtitle>
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Nesciunt dicta aperiam, numquam voluptatibus atque assumenda 
                  </v-list-item-subtitle>
                </v-list-item>


              </v-list>
            </v-card>
        </v-menu>

        <v-menu>
            <template #activator="{ props }">
              <v-avatar v-bind="props">
                <v-img cover src="https://i.pinimg.com/474x/f9/ce/18/f9ce1862e47d5134aa16728c06309f2e.jpg"></v-img>
              </v-avatar>
            </template>

            <v-card min-width="200px">
              <v-list nav density="compact" :lines="false"> 

                <v-list-item prepend-icon="mdi-account-outline">
                  <v-list-item-title>Meu perfil</v-list-item-title>
                </v-list-item>

                <v-list-item prepend-icon="mdi-heart-outline">
                  <v-list-item-title>Favoritos</v-list-item-title>
                </v-list-item>

              </v-list>
            </v-card>
        </v-menu>

      </template>
      <v-app-bar-title>Meu app</v-app-bar-title>
    </v-app-bar>

    <v-main>
      <v-container>
        <h2 class="mb-6">Dashboard</h2>

        <v-card flat class="border mb-6">
          <v-card-title>Últimos usuátios</v-card-title>
          <v-table
          >
            <thead>
              <tr>
                <th>Nome</th>
                <th>Email</th>
                <th>Cargo</th>
                <th>Ações</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td>Nicolas</td>
                <td>nickpupu@gmail.com</td>
                <td>Analista de UX/UI</td>
                <td>
                  <v-btn icon="mdi-pencil" color="primary" variant="text"></v-btn>
                </td>
              </tr>
              <tr>
                <td>Gustavo</td>
                <td>gus.delcoli@gmail.com</td>
                <td>Desenvolvedor</td>
                <td>
                  <v-btn icon="mdi-pencil" color="primary" variant="text"></v-btn>
                </td>
              </tr>
              <tr>
                <td>Gabriel</td>
                <td>email.gabriel@gmail.com</td>
                <td>Tech Lead</td>
                <td>
                  <v-btn icon="mdi-pencil" color="primary" variant="text"></v-btn>
                </td>
              </tr>
            </tbody>
          </v-table>
        </v-card>

        
        <v-row>

          <v-col cols="12" sm="6" md="4" lg="3">
            <v-card>
              <v-img cover class="align-end text-white" src="https://images.pexels.com/photos/4388167/pexels-photo-4388167.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1">
                <v-card-title>Cidade perdida</v-card-title>
              </v-img>

              <v-card-subtitle class="pt-3">Wadi Musa</v-card-subtitle>

              <v-card-text>
                <div>Antiga Construção Em Pedra De Cidade Em Ruínas</div>
                <div>Wadi Musa, Ma'an Governorate, Jordan</div>
              </v-card-text>

              <v-card-actions>
                <v-btn color="primary" variant="outlined">Ver mais</v-btn>
                <v-btn color="blue" variant="tonal" prepend-icon="mdi-cart">Comprar</v-btn>
              </v-card-actions>

            </v-card>
          </v-col>

          <v-col cols="12" sm="6" md="4" lg="3">
            <v-card>
              <v-img cover class="align-end text-white" src="https://images.pexels.com/photos/4388167/pexels-photo-4388167.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1">
                <v-card-title>Cidade perdida</v-card-title>
              </v-img>

              <v-card-subtitle class="pt-3">Wadi Musa</v-card-subtitle>

              <v-card-text>
                <div>Antiga Construção Em Pedra De Cidade Em Ruínas</div>
                <div>Wadi Musa, Ma'an Governorate, Jordan</div>
              </v-card-text>

              <v-card-actions>
                <v-btn color="primary" variant="outlined">Ver mais</v-btn>
                <v-btn color="blue" variant="tonal" prepend-icon="mdi-cart">Comprar</v-btn>
              </v-card-actions>

            </v-card>
          </v-col>

          <v-col cols="12" sm="6" md="4" lg="3">
            <v-card>
              <v-img cover class="align-end text-white" src="https://images.pexels.com/photos/4388167/pexels-photo-4388167.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1">
                <v-card-title>Cidade perdida</v-card-title>
              </v-img>

              <v-card-subtitle class="pt-3">Wadi Musa</v-card-subtitle>

              <v-card-text>
                <div>Antiga Construção Em Pedra De Cidade Em Ruínas</div>
                <div>Wadi Musa, Ma'an Governorate, Jordan</div>
              </v-card-text>

              <v-card-actions>
                <v-btn color="primary" variant="outlined">Ver mais</v-btn>
                <v-btn color="blue"  variant="tonal" prepend-icon="mdi-cart">Comprar</v-btn>
              </v-card-actions>

            </v-card>
          </v-col>

          <v-col cols="12" sm="6" md="4" lg="3">
            <v-card>
              <v-img cover class="align-end text-white" src="https://images.pexels.com/photos/4388167/pexels-photo-4388167.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1">
                <v-card-title>Cidade perdida</v-card-title>
              </v-img>

              <v-card-subtitle class="pt-3">Wadi Musa</v-card-subtitle>

              <v-card-text>
                <div>Antiga Construção Em Pedra De Cidade Em Ruínas</div>
                <div>Wadi Musa, Ma'an Governorate, Jordan</div>
              </v-card-text>

              <v-card-actions>
                <v-btn color="primary" variant="outlined">Ver mais</v-btn>
                <v-btn color="blue"  variant="tonal" prepend-icon="mdi-cart">Comprar</v-btn>
              </v-card-actions>

            </v-card>
          </v-col>
          
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script setup>
import { ref } from 'vue';

  const isDrawerOpen = ref(false)
</script>
