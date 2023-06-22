<template>
    <v-row>
        <v-col cols="7">
            <v-card class="mb-1">
                <v-card-title>Developing Knowledge and Skills</v-card-title>
                <v-card-subtitle class="pb-0">You develop new knowledge and skills that are valuable to your development and your personal purpose. You professionally provide evidence of this relevance and demonstrate your growth.</v-card-subtitle>
                <v-row>
                    <v-col>
                        <v-card-text>
                            <v-icon>mdi-printer-3d</v-icon> 
                            This minor was the first time I worked with 3D modelling and printing. 
                            I learned how to use Fusion 360 to create 3D models for my 11 pin connector and project box.
                            The instructions in the makerspace taught me how to use the 3D printers to print them.
                            Being able to design and print the connector itself saved me a lot of time and money, as that part is only manufactured in the USA and pricing was insane.
                            I did learn some interesting lessons in this process: always check your measurements and tolerances, and <b>never</b> use hot glue on PLA.
                            <br><br>
                            <v-icon>mdi-chip</v-icon>
                            Even though I was already accustomed to programming for Arduino, I learned a lot more about microcontrollers this semester.
                            Since I wanted to make my cassette deck controller wireless and after doing some research, I found that the ESP32 was the best fit for the job.
                            I learned how to program the ESP32 and how to use it to communicate wirelessly with my laptop and phone using Bluetooth, Bluetooth Low Energy (BLE), and WiFi.
                            There were some hardware limitations which forced me to also learn to program a Raspberry Pi Nano, which was totally different compared to the Arduino and ESP32.
                            In the end, the ESP32 is used to control the relay, handle the Bluetooth audio connection, control the DAC (digital to analog converter), and run the display.
                            The Raspberry Pi Nano is used to host the web interface that sends commands to the ESP32 which are sent to the cassette deck through the relay. 
                            <br><br>
                            <v-icon>mdi-laser-pointer</v-icon>
                            In order to create the wooden cover for the controller box, I learned how to use the laser cutter in the makerspace.
                            By learning how to use Inkscape I was able to recreate the look of the cassette deck case in a smaller form factor. 
                            <br>
                            I also wanted to recreate the iconic brushed aluminum look of the cassette deck.
                            After I translated my design from Inkscape to Fusion 360, I received help from the students at Nexus to laser cut aluminum for the face plate.                             
                            <br><br>
                            <v-icon>mdi-soldering-iron</v-icon>
                            Soldering is something I've done in the past, but due to my unsteady hands I've never been very good at it. 
                            The proper soldering irons and soldering stations in the makerspace made it a lot easier for me to solder to PCB's, connectors, and wires.
                            I also learned how to use a multimeter and oscilloscope to troubleshoot my circuitry, which was very useful when I was trying to figure out where my cable break was located.
                            <br><br>
                            <v-icon>mdi-hand-saw</v-icon>
                            Although I already had some experience with woodworking, this project required me learn a new skill: veneering.
                            Compared to the more traditional woodworking I had done before, veneering is way more delicate and requires a lot of patience.
                            By following some tutorials online, I was able to veneer the wooden cover for the controller box.
                            In a hurry, I used wood glue to attach the veneer to the wood, which spilled out and dried on the veneer.
                            After doing a lot of sanding, treating the wood with linseed oil, resanding, and retreating, I was able to get the veneer to look good but not perfect. 
                            In the future, I will use contact cement to attach the veneer to the wood to mitigate the risk of glue spillage.
                        </v-card-text>
                    </v-col>
                </v-row>
            </v-card>
        </v-col>
        <v-col cols="5">
            <v-card>
                <v-card-text class="pb-0">
                    <v-carousel v-model="selectedPicture" hide-delimiters>
                        <v-carousel-item
                            v-for="(picture, index) in pictures" :key="index"
                        >
                        <v-sheet
                            height="100%"
                            tile
                        >
                            <v-row
                            class="fill-height"
                            align="center"
                            justify="center"
                            >
                                <v-img :src="picture.src" contain max-height="550"></v-img>
                            </v-row>
                        </v-sheet>
                        </v-carousel-item>
                    </v-carousel>
                </v-card-text>
                <v-card-text>
                    {{ pictures[selectedPicture].description }}
                </v-card-text>
            </v-card>
        </v-col>
    </v-row>
    
</template>

<script>

export default {
    components: {
    },
    data: () => ({
        selectedPicture: 0,
        pictures: [
            {
                src: 'https://picsum.photos/seed/1/300/300',
                description: 'Image 1',
            },
            {
                src: 'https://picsum.photos/seed/2/300/300',
                description: 'Image 2',
            },
            {
                src: 'https://picsum.photos/seed/3/300/300',
                description: 'Image 3',
            },
            {
                src: 'https://picsum.photos/seed/4/300/300',
                description: 'Image 4',
            },
            {
                src: 'https://picsum.photos/seed/5/300/300',
                description: 'Image 5',
            },
            {
                src: 'https://picsum.photos/seed/6/300/300',
                description: 'Image 6',
            },
            {
                src: 'https://picsum.photos/seed/7/300/300',
                description: 'Image 7',
            },
            {
                src: 'https://picsum.photos/seed/8/300/300',
                description: 'Image 8',
            },
            {
                src: 'https://picsum.photos/seed/9/300/300',
                description: 'Image 9',
            },
            {
                src: 'https://picsum.photos/seed/10/300/300',
                description: 'Image 10',
            },
            {
                src: 'https://picsum.photos/seed/11/300/300',
                description: 'Image 11',
            },
            {
                src: 'https://picsum.photos/seed/12/300/300',
                description: 'Image 12',
            },
            {
                src: 'https://picsum.photos/seed/13/300/300',
                description: 'Image 13',
            },
            {
                src: 'https://picsum.photos/seed/14/300/300',
                description: 'Image 14',
            },
            {
                src: 'https://picsum.photos/seed/15/300/300',
                description: 'Image 15',
            },
            {
                src: 'https://picsum.photos/seed/16/300/300',
                description: 'Image 16',
            },
            {
                src: 'https://picsum.photos/seed/17/300/300',
                description: 'Image 17',
            }      
        ],
    }),
}
</script>