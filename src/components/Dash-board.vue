<template>
<v-container fluid >
    <v-card color="#564345" height="250px" tile flat class="d-flex align-center justify-center " dark>
        <v-row>
            <v-col cols="12" sm="12" >
                <h4 class="text-center"> mens lifestyle shoes</h4>
            </v-col>
            <v-col cols="12" sm="12">
                <v-breadcrumbs :items="items" class="justify-center mt-n7" dark>
                    <template v-slot:divider>
                        <v-icon color ="#745433">mdi-chevron-right</v-icon>
                    </template>
                </v-breadcrumbs>
            </v-col>
        </v-row>
    </v-card>
    <v-card tile class="mx-16 mt-n10 card1" color="white">
        <v-row>
            <v-col cols="12" sm="8" class="pr-0">
                <v-card height="250px" tile flat  color="#434522">
                    <v-row style="width:100%; height:100%">
                        <v-col cols="12" sm="4" class="pl-8 pt-5">
                            <v-btn color="black" dark class="withoutupercase" small tile>
                                new
                            </v-btn>
                            <h6 class="white--text mt-8">motorbike racing</h6>
                            <h3 class="white--text mt-5">trek speed concept</h3>
                            <v-btn rounded class="withoutuoercase px-8 mt-10" color="#545645" dark>
                                more info
                            </v-btn>
                        </v-col>
                        <v-col cols="12" sm="8" style="width:100%; height:100%">
                            <!-- <v-img src="bike.jpg" max-height="400" max-width="400" contain class="mt-n3"></v-img> -->
                            <img src="bike.jpg" alt="" style="max-height:100%" onload="camouflage(this)">
                        </v-col>
                    </v-row>
                </v-card>
            </v-col>
            <v-col cols="12" sm="4" class="pl-0">
                <v-card height="250px" tile flat color="#684534">
                    <v-row>
                        <v-col cols="12" sm="6" class="pl-8 pt-5">
                            <v-btn color="black" dark class="withoutupercase" small tile>
                                new
                            </v-btn>
                            <h6 class="white--text mt-8">DOWN JACKET</h6>
                            <h3 class="white--text mt-5">sale collection 2015</h3>
                            <v-btn rounded class="withoutuoercase px-8 mt-10" color="#545645" dark>
                                more info
                            </v-btn>                        
                        </v-col>                       
                        <v-col cols="12" sm="6" class="pt-0">
                            <v-img  style="height:100%" src="jacket.webp" max-width="420" contain class="mt-n2"  ></v-img>
                            <!-- <img src="jacket.webp" alt="" style="height:100%" onload="camouflage(this)"> -->
                        </v-col>
                    </v-row>
                </v-card>
            </v-col>
        </v-row>
        <v-row class="mt-n6">
            <v-col cols="12" sm="3"  class="pr-0 pl-0">
                <v-toolbar flat outlined>
                    <v-toolbar-title><strong>Filter</strong></v-toolbar-title>
                    <v-spacer></v-spacer>
                    <v-divider vertical></v-divider>
                    <v-btn icon class="ml-1">
                        <v-icon color="#385675">
                            mdi-sync
                        </v-icon>

                    </v-btn>
                </v-toolbar>
            </v-col>
            <v-col cols="12" sm="3" class="pr-0 pl-0">
                <v-toolbar flat outlined>
                    <v-toolbar-title>
                        SPORT BY : <span>Price $-$$</span>
                    </v-toolbar-title>
                    <v-spascer></v-spascer>
                    <v-btn icon class="mr-4">
                        <v-icon color="black">mdi-menu-down</v-icon>
                    </v-btn>
                </v-toolbar>
            </v-col>
            <v-col cols="12" sm="3" class="pr-0 pl-0">
                <v-toolbar flat outlined>
                    <v-btn icon class="mr-1">
                        <v-icon color="#383231" >
                            mdi-apps
                        </v-icon>
                    </v-btn>
                    <v-divider vertical></v-divider>
                    <v-btn icon class="mx-1">
                        <v-icon color="#383231">
                            mdi-format-list-bulleted
                        </v-icon>
                    </v-btn>
                    <v-divider vertical></v-divider>
                    <v-toolbar-title class="ml-2">
                        <strong>COMPAR :</strong>
                    </v-toolbar-title>
                    <v-spacer></v-spacer>
                    <v-badge color="#383234" content="3" class="mr-2"></v-badge>
                </v-toolbar>
            </v-col>
            <v-col cols="12" sm="3" class="pr-0 pl-0">
                <v-toolbar flat outlined>
                    <v-toolbar-title>SHOW : <span>12</span></v-toolbar-title>
                    <v-spacer></v-spacer>
                     <v-btn icon class="mr-4">
                        <v-icon color="black" >mdi-menu-down</v-icon>
                        </v-btn>   
                        </v-toolbar>
            </v-col>
            <v-col cols="3" sm="3" class="pr-0 pl-0 mt-n6" >
                <v-card flat outlined tile>
                    <v-toolbar flat>
                        <v-icon color="black" class="mr-2">mdi-chevron-down</v-icon>
                        <strong>CATEGORIES</strong>
                        <v-spacer></v-spacer>
                        <v-icon color="grey" small>
                            mdi-close

                        </v-icon>
                    </v-toolbar>
                    <v-list dense class="mt-n5">
                        <v-list-item v-for="style in styles" :key="style.title">
                            <v-list-item-content>
                                <v-list-item-title v-text="style.title" class="ml-8"></v-list-item-title>
                            </v-list-item-content>
                            <v-list-item-action>
                                <v-list-item-subtitle v-text="style.count"></v-list-item-subtitle>
                            </v-list-item-action>
                        </v-list-item>
                    </v-list>
                </v-card>
                <v-card flat outlined tile>
                    <v-toolbar flat>
                        <v-icon color="black" class="mr-2">mdi-chevron-down</v-icon>
                        <strong>PRICE</strong>
                        <v-spacer></v-spacer>
                        <v-icon color="grey" small>mdi-close</v-icon>
                    </v-toolbar>
                    <v-toolbar flat>
                        <v-text-field placeholder="$50" filled rounded dense class="mx-2" ></v-text-field>
                        <v-text-field placeholder="$1900" filled rounded dense class="mx-2" ></v-text-field>
                    </v-toolbar>
                    <v-range-slider color="blue" max="40" min="-30"></v-range-slider>

                </v-card>
                <v-card flat outlined tile>
                    <v-toolbar flat>
                    <v-icon color="black" class="mr-2">mdi-chevron-down</v-icon>
                    <strong>BRAND</strong>
                    <v-spacer></v-spacer>
                    <v-icon color="grey" small>mdi-close</v-icon>
                    </v-toolbar>
                    <v-list class="mt-n5">
                        <v-list-item v-for="brand in brands"  :key="brand.title" >
                            <v-list-item-content >
                            <v-list-item-title v-text="brand.title" class="ml-6"></v-list-item-title>
                            </v-list-item-content>
                            <v-list-item-action >
                                <v-checkbox color="primary" v-model="brand.status"></v-checkbox>
                            </v-list-item-action>
                        </v-list-item> 
                    </v-list>
                </v-card>
                 <v-card flat outlined tile>
                    <v-toolbar flat>
                    <v-icon color="black" class="mr-2">mdi-chevron-down</v-icon>
                    <strong>COLOR</strong>
                    <v-spacer></v-spacer>
                    <v-icon color="grey" small>mdi-close</v-icon>
                    </v-toolbar>
                    <v-chip-group column multiple class="pl-2"> 
                        <v-chip filter outlined color="black" text-color="black"></v-chip>
                        <v-chip filter  color="red" text-color="white"  ></v-chip>
                        <v-chip filter  color="green" text-color="white" ></v-chip>
                        <v-chip filter  color="yellow" text-color="white" ></v-chip>
                        <v-chip filter  color="brown" text-color="white" ></v-chip>
                        <v-chip filter  color="blue" text-color="white" ></v-chip>
                        <v-chip filter  color="red" text-color="white"  ></v-chip>
                        <v-chip filter  color="lime" text-color="white" ></v-chip>
                        <v-chip filter  color="grey" text-color="white" ></v-chip>
                        <v-chip filter  color="black" text-color="white" ></v-chip>
                        <v-chip filter  color="red" text-color="white" ></v-chip>
                        <v-chip filter  color="orange" text-color="white" ></v-chip>
                        <v-chip filter  color="pink" text-color="white" ></v-chip>
                        <v-chip filter  color="#f76853" text-color="white" ></v-chip>
                        <v-chip filter  color="#f76432" text-color="white" ></v-chip>
                        <v-chip filter  color="#abc432" text-color="white" ></v-chip>
                        <v-chip filter  color="#877543" text-color="white" ></v-chip>
                        <v-chip filter  color="#e4e323" text-color="white" ></v-chip>
                        <v-chip filter  color="#987f43" text-color="white" ></v-chip>
                        <v-chip filter  color="#980f13" text-color="white" ></v-chip>
                        <v-chip filter  color="#9c0f13" text-color="white" ></v-chip>
                        <v-chip filter  color="#9c5433" text-color="white" ></v-chip>
                        <v-chip filter  color="#334575" text-color="white" ></v-chip>
                        <v-chip filter  color="#d1237f" text-color="white" ></v-chip>
                    </v-chip-group>
                </v-card>
                 <v-card flat outlined tile>
                    <v-toolbar flat>
                    <v-icon color="black" class="mr-2">mdi-chevron-down</v-icon>
                    <strong>SIZE</strong>
                    <v-spacer></v-spacer>
                    <v-icon color="grey" small>mdi-close</v-icon>
                    </v-toolbar>
                    <v-chip-group column multiple active-class="blue white--text" class="pl-2"  > 
                        <v-chip v-for="size in sizes" :key="size" :value="size" class="size">
                            {{size}}
                        </v-chip>
                    </v-chip-group>
                </v-card>
            </v-col>
            <v-col cols="9"  class="pr-0 pl-0 mt-n3 ">
                <v-row  class="px-3">
                    <v-col cols="12" sm="4" v-for="(clothe,i) in clothes" :key="i" :class="clothe.class">
                        <v-hover v-slot:default="{hover}">
                            <v-card height="300" align="center" flat outlined tile>
                                <v-card-action>
                                <v-spacer></v-spacer>
                                <v-btn color="black" small dark>{{clothe.sold}}</v-btn>
                            </v-card-action>
                            <v-img :src=clothe.image width="200" height="200" contain  ></v-img>
                            <v-card-text class="mt-n4">
                                <strong :class=" hover ? 'red--text' : 'black--text'">
                                    {{clothe.title}}
                                </strong>
                            </v-card-text>
                            <v-expand-transition>
                                <div v-if="hover" class="d-flex transition-fast-in-fast-out blue v-card--reveal display-3 white--text" style="height:100%;" > 
                                    <v-btn rounded color="white">
                                        <v-icon>mdi-cart-outline</v-icon>
                                        Buy
                                    </v-btn>
                                    <v-btn fab small color="white" class="ml-2">
                                        <v-icon color="black">
                                            mdi-content-copy

                                        </v-icon>
                                    </v-btn>
                                    <v-btn fab small color="white" class="ml-2">
                                        <v-icon color="black">
                                            mdi-heart-outline
                                        </v-icon>
                                    </v-btn>
                                </div>
                            </v-expand-transition>
                            </v-card>
                        </v-hover>
                    </v-col>
                </v-row>
            </v-col>
            <v-col cols="12" sm="3" class="mt-n3 pr-0 pl-0 pb-0">
                <v-toolbar flat outlined>
                </v-toolbar>
            </v-col>
            <v-col cols="12" sm="3" class="mt-n3 pr-0 pl-0 pb-0">
                <v-toolbar flat outlined>
                    <v-btn icon class="mr-1">
                        <v-icon color="grey">
                            mdi-chevron-up
                        </v-icon>
                        <v-divider vertical></v-divider>
                    </v-btn>
                </v-toolbar>
            </v-col>
            <v-col cols="12" sm="3" class="mt-n3 pr-0 pl-0 pb-0">
                <v-toolbar flat outlined class="text-center">
                    <v-pagination v-model="page" :length="4"></v-pagination>
                </v-toolbar>
            </v-col>
            <v-col cols="12" sm="3" class="mt-n3 pl-0 pr-0  pb-0">
                <v-toolbar flat outlined>
                    <v-btn icon class="mr-1">
                        <v-icon color="grey">
                            mdi-chevron-down
                        </v-icon>
                        <v-divider vertical></v-divider>
                    </v-btn>
                </v-toolbar>
            </v-col>
        </v-row>
    </v-card>
    <v-card color="#EFF0F2" height="250xp" tile flat dark class="d-flex align-center justify-center mt-n5 card2">
                <v-row>
                    <v-col cols="12" sm="12">
                        <h4 class="text-center black--text mt-10">SUBSCRIBE TO OUR NEWSLETER</h4>

                    </v-col>
                    <v-col cols="12" sm="12">
                        <h6 class="text-center grey--text"> Vue.js is awesome</h6>
                    </v-col>
                    <v-col cols="12" sm="12">
                        <v-card flat color="transparent" class="d-flex justify-center">
                            <v-text-field placeholder="Enter Your Email" rounded class=" shrink" background-color="grey" filled append-icon="mdi-email-outline" dense></v-text-field>
                        </v-card>
                    </v-col>
                </v-row>
            </v-card>
</v-container>


</template>

<script>
export default {
data : () => ({
   page : 1, 
   items : [
        {
            text:"Home",
            disabled:false,
            herf:'breadcrumb_home',
        },
        {
            text:"Catalog",
            disabled:false,
            herf:'breadcrumb_catalog',
        },
        {
            text:"Men",
            disabled:false,
            herf:'breadcrumb_men',
        },
        {
            text:"Shoes",
            disabled:false,
            herf:'breadcrumb_shoes',
        },

    ],
    styles : [
        {
            title:'basketball',
            count:'30'

        },
                {
            title:'golf',
            count:'34'

        },
                {
            title:'vollyball',
            count:'21'

        },
                {
            title:'tenes',
            count:'56'

        },
                {
            title:'football',
            count:'53'

        },

    ],
     brands : [
        {
            title:'Lifestyles',
            status:true

        },
                {
            title:'Running',
            status:false

        },
                {
            title:'Training',
            status:false

        },
                {
            title:'Football',
            status:true

        },

    ],
    clothes : [
        {
            class:'pa-0',
            sold:'-20%',
            image:'1.webp',
            title:'KD 8 EXT',
            price:'$ 145.00'
        },
                {
            class:'pa-0',
            sold:'-20%',
            image:'2.webp',
            title:'KD 8 EXT',
            price:'$ 145.00'
        },
                {
            class:'pa-0',
            sold:'-20%',
            image:'3.avif',
            title:'KD 8 EXT',
            price:'$ 145.00'
        },
                {
            class:'pa-0',
            sold:'-20%',
            image:'4.jpg',
            title:'KD 8 EXT',
            price:'$ 145.00'
        },
                {
            class:'pa-0',
            sold:'-20%',
            image:'5.jpg',
            title:'KD 8 EXT',
            price:'$ 145.00'
        },
                {
            class:'pa-0',
            sold:'-20%',
            image:'6.jpg',
            title:'KD 8 EXT',
            price:'$ 145.00'
        },
                {
            class:'pa-0',
            sold:'-20%',
            image:'7.jpg',
            title:'KD 8 EXT',
            price:'$ 145.00'
        },
                {
            class:'pa-0',
            sold:'-20%',
            image:'8.jpg',
            title:'KD 8 EXT',
            price:'$ 145.00'
        },
                {
            class:'pa-0',
            sold:'-20%',
            image:'9.jpg',
            title:'KD 8 EXT',
            price:'$ 145.00'
        },
                {
            class:'pa-0',
            sold:'-20%',
            image:'10.jpg',
            title:'KD 8 EXT',
            price:'$ 145.00'
        },

                {
            class:'pa-0',
            sold:'-20%',
            image:'11.jpg',
            title:'KD 8 EXT',
            price:'$ 145.00'
        },
                {
            class:'pa-0',
            sold:'-20%',
            image:'12.jpg',
            title:'KD 8 EXT',
            price:'$ 145.00'
        },
                {
            class:'pa-0',
            sold:'-20%',
            image:'13.webp',
            title:'KD 8 EXT',
            price:'$ 145.00'
        },
                {
            class:'pa-0',
            sold:'-20%',
            image:'14.webp',
            title:'KD 8 EXT',
            price:'$ 145.00'
        },
                {
            class:'pa-0',
            sold:'-20%',
            image:'15.jpg',
            title:'KD 8 EXT',
            price:'$ 145.00'
        },
                {
            class:'pa-0',
            sold:'-20%',
            image:'16.jpg',
            title:'KD 8 EXT',
            price:'$ 145.00'
        },
                {
            class:'pa-0',
            sold:'-20%',
            image:'17.jpg',
            title:'KD 8 EXT',
            price:'$ 145.00'
        },
                {
            class:'pa-0',
            sold:'-20%',
            image:'18.jpg',
            title:'KD 8 EXT',
            price:'$ 145.00'
        },

    ],
    sizes : ['32','33', '34','35','36','37','38','39','40','41','42','43','44','45','46','47','48','49' ]
})

}
</script>

<style>
.container{
    padding: 0% !important;
}
.v-btn.withoutuoercase{
    text-decoration: none;
}
.v-chip.v-size--default {
    border-radius: 50px !important;
    font-size: 14px !important;
    height: 40px !important;
    width: 40px !important;

}
.v-card--reveal{
    align-items: center;
    bottom: 0%;
    justify-content: center;
    opacity: .5;
    position: absolute;
    width: 100%;

}

.card1{
    z-index:10 ;
}
.card2{
    z-index: 1;
}
</style>