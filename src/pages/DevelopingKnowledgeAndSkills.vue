<template>
    <v-row>
        <v-col cols="5">
            <PictureCarousel :pictures="pictures"/>
        </v-col>
        <v-col cols="7">
            <v-card class="mb-1">
                <v-card-title>Developing Knowledge and Skills</v-card-title>
                <v-card-subtitle class="pb-0">You develop new knowledge and skills that are valuable to your development and your personal purpose. You professionally provide evidence of this relevance and demonstrate your growth.</v-card-subtitle>
                <v-row>
                    <v-col>
                        <v-card-text>
                            <v-icon color="amber darken-3">mdi-printer-3d</v-icon> 
                            This minor was the first time I worked with 3D modeling and printing. 
                            I learned how to use Fusion 360 to create 3D models for my 11 pin connector and project box.
                            The instructions in the makerspace taught me how to use the 3D printers to print them.
                            Being able to design and print the connector itself saved me a lot of time and money, as that part is only manufactured in the USA and pricing was insane.
                            I did learn some interesting lessons in this process: always check your measurements and tolerances, and <b>never</b> use hot glue on PLA.
                            <br><br>
                            <v-icon color="amber darken-2">mdi-chip</v-icon>
                            Even though I was already accustomed to programming for Arduino, I learned a lot more about microcontrollers this semester.
                            Since I wanted to make my cassette deck controller wireless and after doing some research, I found that the ESP32 was the best fit for the job.
                            I learned how to program the ESP32 and how to use it to communicate wirelessly with my laptop and phone using Bluetooth, Bluetooth Low Energy (BLE), and WiFi.
                            There were some hardware limitations which forced me to also learn to program a Raspberry Pi Nano, which was totally different compared to the Arduino and ESP32.
                            In the end, the ESP32 is used to control the relay, handle the Bluetooth audio connection, control the DAC (digital to analog converter), and run the display.
                            The Raspberry Pi Nano is used to host the web interface that sends commands to the ESP32 which are sent to the cassette deck through the relay. 
                            <br><br>
                            <v-icon color="amber darken-1">mdi-soldering-iron</v-icon>
                            Soldering is something I've done in the past, but due to my unsteady hands I've never been very good at it. 
                            The proper soldering irons and soldering stations in the makerspace made it a lot easier for me to solder to PCB's, connectors, and wires.
                            I also learned how to use a multimeter and oscilloscope to troubleshoot my circuitry, which was very useful when I was trying to figure out where a cable break was located.
                            <br><br>
                            <v-icon color="amber">mdi-laser-pointer</v-icon>
                            In order to create the wooden cover for the controller box, I learned how to use the laser cutter in the makerspace.
                            By learning how to use Inkscape I was able to recreate the look of the cassette deck case in a smaller form factor. 
                            <br>
                            I also wanted to recreate the iconic brushed aluminum look of the cassette deck.
                            After I translated my design from Inkscape to Fusion 360, I received help from the students at Nexus to laser cut aluminum for the face plate.                             
                            <br><br>
                            <v-icon color="amber lighten-1">mdi-hand-saw</v-icon>
                            Although I already had some experience with woodworking, this project required me to learn a new skill: veneering.
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
    </v-row>
    
</template>

<script>
import PictureCarousel from '@/components/PictureCarousel.vue'

export default {
    components: {
        PictureCarousel
    },
    data: () => ({
        pictures: [
            {
                src: "/slides/3_developing_knowledge_and_skills/3d_printing_1.jpeg",
                description: "Three prototypes of the 11 pin connector. The black one was too small, the white one didn't have enough space for the pins, the yellow one was exactly what I needed.",
            },
            {
                src: "/slides/3_developing_knowledge_and_skills/3d_printing_2.jpeg",
                description: "Three prototypes of the 11 pin connector. The black one was too small, the white one didn't have enough space for the pins, the yellow one was exactly what I needed.",
            },
            {
                src: "/slides/3_developing_knowledge_and_skills/3d_printing_3.jpeg",
                description: "Sanding down the first prototype of the controller box to fix some tolerance issues.",
            },
            {
                src: "/slides/3_developing_knowledge_and_skills/microcontroller_3.jpeg",
                description: "Controlling the relay with the ESP32."
            },
            {
                src: "/slides/3_developing_knowledge_and_skills/microcontroller_1.jpeg",
                description: "Testing the Bluetooth audio connection with the ESP32 using its internal DAC (digital to analog converter)."
            },
            {
                src: "/slides/3_developing_knowledge_and_skills/microcontroller_2.jpeg",
                description: "Testing the Bluetooth audio connection with the ESP32 using an external DAC (digital to analog converter) for improved audio quality."
            },
            {
                src: "/slides/3_developing_knowledge_and_skills/microcontroller_4.jpeg",
                description: "Programming the the display that shows the track and artist you are recording. This data is sent from the connected Bluetooth device and processed by the ESP32."
            },
            {
                src: "/slides/3_developing_knowledge_and_skills/soldering_1.jpeg",
                description: "Soldering the buttons together on the paper prototype."
            },
            {
                src: "/slides/3_developing_knowledge_and_skills/soldering_2.jpeg",
                description: "Testing the connections of the paper prototype with a multimeter."
            },
            {
                src: "/slides/3_developing_knowledge_and_skills/soldering_3.jpeg",
                description: "Testing the quality of the internal DAC (digital to analog converter) of the ESP32 using an oscilloscope."
            },
            {
                src: "/slides/3_developing_knowledge_and_skills/soldering_4.jpeg",
                description: "Soldering audio jacks to the external DAC (digital to analog converter) PCB."
            },
            {
                src: "/slides/3_developing_knowledge_and_skills/soldering_5.jpeg",
                description: "Soldering audio jacks to the external DAC (digital to analog converter) PCB."
            },
            {
                src: "/slides/3_developing_knowledge_and_skills/laser_cutting_1.jpeg",
                description: "The laser cut MDF cover pieces, fresh from the laser cutter."
            },
            {
                src: "/slides/3_developing_knowledge_and_skills/laser_cutting_2.jpeg",
                description: "The assembled laser cut wooden cover. The wood glue was still drying."
            },
            {
                src: "/slides/3_developing_knowledge_and_skills/laser_cutting_3.jpeg",
                description: "The wooden cover after sanding."
            },
            {
                src: "/slides/3_developing_knowledge_and_skills/laser_cutting_4.jpeg",
                description: "The laser cut aluminium face plate and its wooden test piece."
            },
            {
                src: "/slides/3_developing_knowledge_and_skills/woodworking_1.jpeg",
                description: "Cutting the veneer to size."
            },
            {
                src: "/slides/3_developing_knowledge_and_skills/woodworking_2.jpeg",
                description: "Applying the veneer to the wooden cover."
            },
            {
                src: "/slides/3_developing_knowledge_and_skills/woodworking_3.jpeg",
                description: "The wooden cover before sanding and treating with linseed oil (ventilation slits not yet cut)."
            },
            {
                src: "/slides/3_developing_knowledge_and_skills/woodworking_4.jpeg",
                description: "The wooden cover after sanding while the linseed oil was drying (ventilation slits were cut)."
            },
            {
                src: "/slides/3_developing_knowledge_and_skills/woodworking_5.jpeg",
                description: "The woorden cover after the initial treatment. The blemishes from the wood glue are still visible around the edges on the top."
            },
        ],
    }),
}
</script>