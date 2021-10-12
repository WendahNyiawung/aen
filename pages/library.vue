<template>
  <v-row>
    <v-col class="text-center">
      <v-card class="mb-3 pb-3" elevation="0">
        <div class="card-container px-1 rounded-0 d-flex justify-space-between">
          <v-breadcrumbs :items="items" divider="/" large></v-breadcrumbs>
          <a
            class="card-link mt-4 me-2"
            href="https://africaeducationnetwork.s3.us-east-2.amazonaws.com/Manuals/AEN+USER+GUIDE+ORIGINAL1.pdf"
            target="_blank"
            rel="noopener noreferrer"
            >Help</a
          >
        </div>
      </v-card>
      <v-card flat class="mt-4 pa-5">
        <v-card-title class="mb-5">
          <v-card class="pa-4">
            <div class="body-2 text--accent-4 grey--text">
              All Our Collections
            </div>
          </v-card>
          <v-spacer></v-spacer>
          <v-text-field
            v-model="search"
            append-icon="mdi-magnify"
            label="Search"
            single-line
            hide-details
          ></v-text-field>
        </v-card-title>
        <v-row>
            <v-col>
               <v-card class="pa-3">
                   <a href="https://catalog.gpo.gov/F/?func=direct&doc_number=000848813&format=999" target="_blank" rel="noopener noreferrer" class="card-link text-left">Gulf of Mexico a focus on community recovery ... </a>
                   <v-row class="mt-4">
                       <v-col >
                           <div class="body-2 mb-3 text-left">Format:</div>
                           <div class="body-2 mb-8 text-left">Main Author:</div>
                           <div class="body-2 mb-3 text-left">Published/Created:</div>
                           <div class="body-2 mb-3 text-left">Link: </div> 
                       </v-col>
                       <v-col md="8">
                           <div class="body-2 mb-3 text-left">text</div>
                           <div class="body-2 mb-3 text-left">United States. Congress. House. Committee on Natural Resources</div>
                           <div class="body-2 mb-3 text-left">Washington : U.S. G.P.O.</div>
                           <div class="body-2 mb-3 text-left">
                             <a href="https://catalog.gpo.gov/F/?func=direct&doc_number=000848813&format=999" target="_blank" rel="noopener noreferrer">https://catalog.gpo.gov/F/?func=direct&doc_number=000848813&format=999</a>   
                            </div> 
                       </v-col>
                       
                   </v-row>
               </v-card>
            </v-col>
            <v-col>
               <v-card class="pa-3">
                   <a href="https://catalog.gpo.gov/F/?func=direct&doc_number=000848813&format=999" target="_blank" rel="noopener noreferrer" class="card-link text-left">Oversight of United States Immigration and Cu...  </a>
                   <v-row class="mt-4">
                       <v-col >
                           <div class="body-2 mb-3 text-left">Format:</div>
                           <div class="body-2 mb-8 text-left">Main Author:</div>
                           <div class="body-2 mb-3 text-left">Published/Created:</div>
                           <div class="body-2 mb-3 text-left">Link: </div> 
                       </v-col>
                       <v-col md="8">
                           <div class="body-2 mb-3 text-left">text</div>
                           <div class="body-2 mb-3 text-left">United States. Congress. House. Committee on the Judiciary, author</div>
                           <div class="body-2 mb-3 text-left">Washington : U.S. Government Publishing Office</div>
                           <div class="body-2 mb-3 text-left">
                             <a href="https://catalog.gpo.gov/F/?func=direct&doc_number=000848813&format=999" target="_blank" rel="noopener noreferrer">https://catalog.gpo.gov/F/?func=direct&doc_number=000848813&format=999</a>   
                            </div> 
                       </v-col>
                       
                   </v-row>
               </v-card>
            </v-col>
            
        </v-row>
        <v-row>
            <v-col>
               <v-card class="pa-3">
                   <a href="https://catalog.gpo.gov/F/?func=direct&doc_number=000848813&format=999" target="_blank" rel="noopener noreferrer" class="card-link text-left">Essays in the economic implications of select...  </a>
                   <v-row class="mt-4">
                       <v-col >
                           <div class="body-2 mb-3 text-left">Format:</div>
                           <div class="body-2 mb-8 text-left">Main Author:</div>
                           <div class="body-2 mb-3 text-left">Published/Created:</div>
                           <div class="body-2 mb-3 text-left">Link: </div> 
                       </v-col>
                       <v-col md="8">
                           <div class="body-2 mb-3 text-left">text</div>
                           <div class="body-2 mb-3 text-left">Cozzens, Tyler William</div>
                           <div class="body-2 mb-3 text-left">Washington : U.S. G.P.O.</div>
                           <div class="body-2 mb-3 text-left">
                             <a href="https://catalog.gpo.gov/F/?func=direct&doc_number=000848813&format=999" target="_blank" rel="noopener noreferrer">https://catalog.gpo.gov/F/?func=direct&doc_number=000848813&format=999</a>   
                            </div> 
                       </v-col>
                       
                   </v-row>
               </v-card>
            </v-col>
            <v-col>
               <v-card class="pa-3">
                   <a href="https://catalog.gpo.gov/F/?func=direct&doc_number=000848813&format=999" target="_blank" rel="noopener noreferrer" class="card-link text-left">Oversight of United States Immigration and Cu...  </a>
                   <v-row class="mt-4">
                       <v-col >
                           <div class="body-2 mb-3 text-left">Format:</div>
                           <div class="body-2 mb-8 text-left">Main Author:</div>
                           <div class="body-2 mb-3 text-left">Published/Created:</div>
                           <div class="body-2 mb-3 text-left">Link: </div> 
                       </v-col>
                       <v-col md="8">
                           <div class="body-2 mb-3 text-left">text</div>
                           <div class="body-2 mb-3 text-left">United States. Congress. House. Committee on the Judiciary, author</div>
                           <div class="body-2 mb-3 text-left">Washington : U.S. Government Publishing Office</div>
                           <div class="body-2 mb-3 text-left">
                             <a href="https://catalog.gpo.gov/F/?func=direct&doc_number=000848813&format=999" target="_blank" rel="noopener noreferrer">https://catalog.gpo.gov/F/?func=direct&doc_number=000848813&format=999</a>   
                            </div> 
                       </v-col>
                       
                   </v-row>
               </v-card>
            </v-col>
            
        </v-row>
        <v-row>
            <v-col>
               <v-card class="pa-3">
                   <a href="https://catalog.gpo.gov/F/?func=direct&doc_number=000848813&format=999" target="_blank" rel="noopener noreferrer" class="card-link text-left">Essays in the economic implications of select...  </a>
                   <v-row class="mt-4">
                       <v-col >
                           <div class="body-2 mb-3 text-left">Format:</div>
                           <div class="body-2 mb-8 text-left">Main Author:</div>
                           <div class="body-2 mb-3 text-left">Published/Created:</div>
                           <div class="body-2 mb-3 text-left">Link: </div> 
                       </v-col>
                       <v-col md="8">
                           <div class="body-2 mb-3 text-left">text</div>
                           <div class="body-2 mb-3 text-left">Cozzens, Tyler William</div>
                           <div class="body-2 mb-3 text-left">Washington : U.S. G.P.O.</div>
                           <div class="body-2 mb-3 text-left">
                             <a href="https://catalog.gpo.gov/F/?func=direct&doc_number=000848813&format=999" target="_blank" rel="noopener noreferrer">https://catalog.gpo.gov/F/?func=direct&doc_number=000848813&format=999</a>   
                            </div> 
                       </v-col>
                       
                   </v-row>
               </v-card>
            </v-col>
            <v-col>
               <v-card class="pa-3">
                   <a href="https://catalog.gpo.gov/F/?func=direct&doc_number=000848813&format=999" target="_blank" rel="noopener noreferrer" class="card-link text-left">Oversight of United States Immigration and Cu...  </a>
                   <v-row class="mt-4">
                       <v-col >
                           <div class="body-2 mb-3 text-left">Format:</div>
                           <div class="body-2 mb-8 text-left">Main Author:</div>
                           <div class="body-2 mb-3 text-left">Published/Created:</div>
                           <div class="body-2 mb-3 text-left">Link: </div> 
                       </v-col>
                       <v-col md="8">
                           <div class="body-2 mb-3 text-left">text</div>
                           <div class="body-2 mb-3 text-left">United States. Congress. House. Committee on the Judiciary, author</div>
                           <div class="body-2 mb-3 text-left">Washington : U.S. Government Publishing Office</div>
                           <div class="body-2 mb-3 text-left">
                             <a href="https://catalog.gpo.gov/F/?func=direct&doc_number=000848813&format=999" target="_blank" rel="noopener noreferrer">https://catalog.gpo.gov/F/?func=direct&doc_number=000848813&format=999</a>   
                            </div> 
                       </v-col>
                       
                   </v-row>
               </v-card>
            </v-col>
            
        </v-row>
        <v-row>
            <v-col>
               <v-card class="pa-3">
                   <a href="https://catalog.gpo.gov/F/?func=direct&doc_number=000848813&format=999" target="_blank" rel="noopener noreferrer" class="card-link text-left">Essays in the economic implications of select...  </a>
                   <v-row class="mt-4">
                       <v-col >
                           <div class="body-2 mb-3 text-left">Format:</div>
                           <div class="body-2 mb-8 text-left">Main Author:</div>
                           <div class="body-2 mb-3 text-left">Published/Created:</div>
                           <div class="body-2 mb-3 text-left">Link: </div> 
                       </v-col>
                       <v-col md="8">
                           <div class="body-2 mb-3 text-left">text</div>
                           <div class="body-2 mb-3 text-left">Cozzens, Tyler William</div>
                           <div class="body-2 mb-3 text-left">Washington : U.S. G.P.O.</div>
                           <div class="body-2 mb-3 text-left">
                             <a href="https://catalog.gpo.gov/F/?func=direct&doc_number=000848813&format=999" target="_blank" rel="noopener noreferrer">https://catalog.gpo.gov/F/?func=direct&doc_number=000848813&format=999</a>   
                            </div> 
                       </v-col>
                       
                   </v-row>
               </v-card>
            </v-col>
            <v-col>
               <v-card class="pa-3">
                   <a href="https://catalog.gpo.gov/F/?func=direct&doc_number=000848813&format=999" target="_blank" rel="noopener noreferrer" class="card-link text-left">Oversight of United States Immigration and Cu...  </a>
                   <v-row class="mt-4">
                       <v-col >
                           <div class="body-2 mb-3 text-left">Format:</div>
                           <div class="body-2 mb-8 text-left">Main Author:</div>
                           <div class="body-2 mb-3 text-left">Published/Created:</div>
                           <div class="body-2 mb-3 text-left">Link: </div> 
                       </v-col>
                       <v-col md="8">
                           <div class="body-2 mb-3 text-left">text</div>
                           <div class="body-2 mb-3 text-left">United States. Congress. House. Committee on the Judiciary, author</div>
                           <div class="body-2 mb-3 text-left">Washington : U.S. Government Publishing Office</div>
                           <div class="body-2 mb-3 text-left">
                             <a href="https://catalog.gpo.gov/F/?func=direct&doc_number=000848813&format=999" target="_blank" rel="noopener noreferrer">https://catalog.gpo.gov/F/?func=direct&doc_number=000848813&format=999</a>   
                            </div> 
                       </v-col>
                       
                   </v-row>
               </v-card>
            </v-col>
            
        </v-row>
      </v-card>
      <div class="text-center">
        <v-pagination v-model="page" :length="6"></v-pagination>
      </div>
    </v-col>
  </v-row>
</template>
<script>
export default {
  data: () => ({
    search: "",
    page: 1,
    items: [
      {
        text: "Home",
        disabled: false,
        href: "/"
      },
      {
        text: "Library Search",
        disabled: true,
        href: "breadcrumbs_link_2"
      }
    ]
  })
};
</script>
<style scoped>
.card-container {
  border-bottom: 4px solid #a2b6c8;
}
.card-link {
  text-decoration: none;
}
.card-link:hover {
  border-bottom: #7ba9ce 1px solid;
}
</style>
