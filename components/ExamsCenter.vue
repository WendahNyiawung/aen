<template>
  <div>
    <v-card flat class="pa-5">
      <div class="d-flex justify-end">
        <div class="text-center">
          <v-dialog v-model="addquestion" width="600">
            <template v-slot:activator="{ on, attrs }">
              <v-btn color="blue lighten-2" dark v-bind="attrs" v-on="on">
                add Questionnaire
              </v-btn>
            </template>

            <v-card>
              <v-card-title class="text-h5 blue white--text">
                Create Questions
                <v-spacer></v-spacer>
                <v-btn color="white" text @click="addquestion = false"
                  >Close</v-btn
                >
              </v-card-title>

              <v-card-text>
                <v-form v-model="valid">
                  <v-container>
                    <v-row>
                      <v-col cols="12" md="6">
                        <v-text-field
                          v-model="title"
                          :rules="nameRules"
                          label="Title"
                          required
                        ></v-text-field>
                      </v-col>
                    </v-row>
                    <v-textarea
                      name="input-7-4"
                      label="Description"
                      v-model="title"
                      :rules="nameRules"
                      required
                    ></v-textarea>
                    <v-label> * indicates required field </v-label>
                  </v-container>
                </v-form>
              </v-card-text>

              <v-card-actions>
                <v-spacer></v-spacer>
                <v-btn color="primary" text @click="addquestion = false">
                  CLOSE
                </v-btn>
                <v-btn color="primary" text @click="addquestion = false">
                  SAVE
                </v-btn>
              </v-card-actions>
            </v-card>
          </v-dialog>
        </div>
      </div>
      <v-card-title class="mb-5">
        Questionnaires
        <v-spacer></v-spacer>
        <v-text-field
          v-model="search"
          append-icon="mdi-magnify"
          label="Search"
          single-line
          hide-details
        ></v-text-field>
      </v-card-title>
      <v-simple-table>
        <template v-slot:default>
          <thead>
            <tr>
              <th class="text-justify">Title</th>
              <th class="text-justify">Subject</th>
              <th class="text-justify">Created By</th>
              <th class="text-justify">Last Date Modified</th>
              <th class="text-justify">Action</th>
            </tr>
          </thead>
          <tbody>
            <tr v-for="item in members" :key="item.name">
              <td class="text-justify">
                <v-btn color="primary" text>{{ item.name }}</v-btn>
              </td>
              <td class="text-justify">
                <v-btn color="primary" text>{{ item.creator }}</v-btn>
              </td>
              <td class="text-justify">{{ item.des }} <br /></td>
              <td class="text-justify">
                {{ item.date }}
              </td>
              <td class="text-justify">
                <div>
                  <v-row>
                    <v-col>
                      <v-row justify="center">
                        <v-dialog
                          v-model="Create"
                          hide-overlay
                          transition="dialog-bottom-transition"
                        >
                          <template v-slot:activator="{ on, attrs }">
                            <v-btn color="green" icon v-bind="attrs" v-on="on">
                              <v-icon>mdi-play-circle-outline </v-icon>
                            </v-btn>
                          </template>
                          <v-card>
                            <v-toolbar dark color="primary">
                              <v-toolbar-title>Exam/Test Center</v-toolbar-title>
                              <v-spacer></v-spacer>
                              <v-toolbar-items>
                                <v-btn dark text @click="Create = false">
                                  Save
                                </v-btn>
                              </v-toolbar-items>
                            </v-toolbar>
                            <v-list three-line subheader>
                              <v-subheader>User Controls</v-subheader>
                              <v-list-item>
                                <v-list-item-content>
                                  <v-list-item-title
                                    >Content filtering</v-list-item-title
                                  >
                                  <v-list-item-subtitle
                                    >Set the content filtering level to restrict
                                    apps that can be
                                    downloaded</v-list-item-subtitle
                                  >
                                </v-list-item-content>
                              </v-list-item>
                              <v-list-item>
                                <v-list-item-content>
                                  <v-list-item-title
                                    >Password</v-list-item-title
                                  >
                                  <v-list-item-subtitle
                                    >Require password for purchase or use
                                    password to restrict
                                    purchase</v-list-item-subtitle
                                  >
                                </v-list-item-content>
                              </v-list-item>
                            </v-list>
                            <v-divider></v-divider>
                            <v-list three-line subheader>
                              <v-subheader>General</v-subheader>
                              <v-list-item>
                                <v-list-item-action>
                                  <v-checkbox
                                    v-model="notifications"
                                  ></v-checkbox>
                                </v-list-item-action>
                                <v-list-item-content>
                                  <v-list-item-title
                                    >Notifications</v-list-item-title
                                  >
                                  <v-list-item-subtitle
                                    >Notify me about updates to apps or games
                                    that I downloaded</v-list-item-subtitle
                                  >
                                </v-list-item-content>
                              </v-list-item>
                              <v-list-item>
                                <v-list-item-action>
                                  <v-checkbox v-model="sound"></v-checkbox>
                                </v-list-item-action>
                                <v-list-item-content>
                                  <v-list-item-title>Sound</v-list-item-title>
                                  <v-list-item-subtitle
                                    >Auto-update apps at any time. Data charges
                                    may apply</v-list-item-subtitle
                                  >
                                </v-list-item-content>
                              </v-list-item>
                              <v-list-item>
                                <v-list-item-action>
                                  <v-checkbox v-model="widgets"></v-checkbox>
                                </v-list-item-action>
                                <v-list-item-content>
                                  <v-list-item-title
                                    >Auto-add widgets</v-list-item-title
                                  >
                                  <v-list-item-subtitle
                                    >Automatically add home screen
                                    widgets</v-list-item-subtitle
                                  >
                                </v-list-item-content>
                              </v-list-item>
                            </v-list>
                          </v-card>
                        </v-dialog>
                      </v-row>
                    </v-col>
                    <v-col>
                      <v-row justify="center">
                        <v-dialog
                          v-model="dialog"
                          hide-overlay
                          transition="dialog-bottom-transition"
                        >
                          <template v-slot:activator="{ on, attrs }">
                            <v-btn color="#3F51B5" icon v-bind="attrs" v-on="on">
                              <v-icon>mdi-forum</v-icon>
                            </v-btn>
                          </template>
                          <v-card>
                            <v-toolbar dark color="primary">
                              <v-btn icon dark @click="dialog = false">
                                <v-icon>mdi-close</v-icon>
                              </v-btn>
                              <v-toolbar-title>Settings</v-toolbar-title>
                              <v-spacer></v-spacer>
                              <v-toolbar-items>
                                <v-btn dark text @click="dialog = false">
                                  Save
                                </v-btn>
                              </v-toolbar-items>
                            </v-toolbar>
                            <v-list three-line subheader>
                              <v-subheader>User Controls</v-subheader>
                              <v-list-item>
                                <v-list-item-content>
                                  <v-list-item-title
                                    >Content filtering</v-list-item-title
                                  >
                                  <v-list-item-subtitle
                                    >Set the content filtering level to restrict
                                    apps that can be
                                    downloaded</v-list-item-subtitle
                                  >
                                </v-list-item-content>
                              </v-list-item>
                              <v-list-item>
                                <v-list-item-content>
                                  <v-list-item-title
                                    >Password</v-list-item-title
                                  >
                                  <v-list-item-subtitle
                                    >Require password for purchase or use
                                    password to restrict
                                    purchase</v-list-item-subtitle
                                  >
                                </v-list-item-content>
                              </v-list-item>
                            </v-list>
                            <v-divider></v-divider>
                            <v-list three-line subheader>
                              <v-subheader>General</v-subheader>
                              <v-list-item>
                                <v-list-item-action>
                                  <v-checkbox
                                    v-model="notifications"
                                  ></v-checkbox>
                                </v-list-item-action>
                                <v-list-item-content>
                                  <v-list-item-title
                                    >Notifications</v-list-item-title
                                  >
                                  <v-list-item-subtitle
                                    >Notify me about updates to apps or games
                                    that I downloaded</v-list-item-subtitle
                                  >
                                </v-list-item-content>
                              </v-list-item>
                              <v-list-item>
                                <v-list-item-action>
                                  <v-checkbox v-model="sound"></v-checkbox>
                                </v-list-item-action>
                                <v-list-item-content>
                                  <v-list-item-title>Sound</v-list-item-title>
                                  <v-list-item-subtitle
                                    >Auto-update apps at any time. Data charges
                                    may apply</v-list-item-subtitle
                                  >
                                </v-list-item-content>
                              </v-list-item>
                              <v-list-item>
                                <v-list-item-action>
                                  <v-checkbox v-model="widgets"></v-checkbox>
                                </v-list-item-action>
                                <v-list-item-content>
                                  <v-list-item-title
                                    >Auto-add widgets</v-list-item-title
                                  >
                                  <v-list-item-subtitle
                                    >Automatically add home screen
                                    widgets</v-list-item-subtitle
                                  >
                                </v-list-item-content>
                              </v-list-item>
                            </v-list>
                          </v-card>
                        </v-dialog>
                      </v-row>
                    </v-col>
                    <v-col>
                      <v-row justify="center">
                        <v-dialog
                          v-model="dialog"
                          hide-overlay
                          transition="dialog-bottom-transition"
                        >
                          <template v-slot:activator="{ on, attrs }">
                            <v-btn color="orange" icon v-bind="attrs" v-on="on">
                              <v-icon>mdi-pencil</v-icon>
                            </v-btn>
                          </template>
                          <v-card>
                            <v-toolbar dark color="primary">
                              <v-btn icon dark @click="dialog = false">
                                <v-icon>mdi-close</v-icon>
                              </v-btn>
                              <v-toolbar-title>Settings</v-toolbar-title>
                              <v-spacer></v-spacer>
                              <v-toolbar-items>
                                <v-btn dark text @click="dialog = false">
                                  Save
                                </v-btn>
                              </v-toolbar-items>
                            </v-toolbar>
                            <v-list three-line subheader>
                              <v-subheader>User Controls</v-subheader>
                              <v-list-item>
                                <v-list-item-content>
                                  <v-list-item-title
                                    >Content filtering</v-list-item-title
                                  >
                                  <v-list-item-subtitle
                                    >Set the content filtering level to restrict
                                    apps that can be
                                    downloaded</v-list-item-subtitle
                                  >
                                </v-list-item-content>
                              </v-list-item>
                              <v-list-item>
                                <v-list-item-content>
                                  <v-list-item-title
                                    >Password</v-list-item-title
                                  >
                                  <v-list-item-subtitle
                                    >Require password for purchase or use
                                    password to restrict
                                    purchase</v-list-item-subtitle
                                  >
                                </v-list-item-content>
                              </v-list-item>
                            </v-list>
                            <v-divider></v-divider>
                            <v-list three-line subheader>
                              <v-subheader>General</v-subheader>
                              <v-list-item>
                                <v-list-item-action>
                                  <v-checkbox
                                    v-model="notifications"
                                  ></v-checkbox>
                                </v-list-item-action>
                                <v-list-item-content>
                                  <v-list-item-title
                                    >Notifications</v-list-item-title
                                  >
                                  <v-list-item-subtitle
                                    >Notify me about updates to apps or games
                                    that I downloaded</v-list-item-subtitle
                                  >
                                </v-list-item-content>
                              </v-list-item>
                              <v-list-item>
                                <v-list-item-action>
                                  <v-checkbox v-model="sound"></v-checkbox>
                                </v-list-item-action>
                                <v-list-item-content>
                                  <v-list-item-title>Sound</v-list-item-title>
                                  <v-list-item-subtitle
                                    >Auto-update apps at any time. Data charges
                                    may apply</v-list-item-subtitle
                                  >
                                </v-list-item-content>
                              </v-list-item>
                              <v-list-item>
                                <v-list-item-action>
                                  <v-checkbox v-model="widgets"></v-checkbox>
                                </v-list-item-action>
                                <v-list-item-content>
                                  <v-list-item-title
                                    >Auto-add widgets</v-list-item-title
                                  >
                                  <v-list-item-subtitle
                                    >Automatically add home screen
                                    widgets</v-list-item-subtitle
                                  >
                                </v-list-item-content>
                              </v-list-item>
                            </v-list>
                          </v-card>
                        </v-dialog>
                      </v-row>
                    </v-col>
                    <v-col>
                      <v-row justify="center">
                   
                      
                            <v-btn color="red" icon >
                              <v-icon>mdi-delete</v-icon>
                            </v-btn>
                        
                      </v-row>
                    </v-col>
                  
                  </v-row>
                </div>
              </td>
            </tr>
          </tbody>
        </template>
      </v-simple-table>
    </v-card>
  </div>
</template>
<script>
export default {
  data() {
    return {
      search: "",
      dialog: false,
      addquestion: false,
      members: [
        {
          name: "Mathematics",
          creator: "lamourette, prof ",
          des: "me ",
          date: "Monday, April 27th 2020",
          action: " ",
        },
        {
          name: "Mathematics",
          creator: "lamourette, prof ",
          des: "user1",
          date: "Monday, April 27th 2020",
          action: " ",
        },
        {
          name: "Mathematics",
          creator: "lamourette, prof ",
          des: "lamourette.student",
          date: "Monday, April 27th 2020",
          action: " ",
        },
      ],
      valid: false,
      title: "",
      nameRules: ["required"],
      Create: false,
       dialog: false,
        notifications: false,
        sound: true,
        widgets: false,
    };
  },
};
</script>
<style scoped>
.table-link {
  text-decoration: none;
  color: #fff;
}
</style>
