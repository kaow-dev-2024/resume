<template>
    <div>
        <v-timeline dense>
            <v-timeline-item v-for="(item, i) in items" :key="i" color="success">
                <v-card>
                    <v-toolbar elevation="0" color="warning" dark>
                        {{ item.start }}-{{ item.end }}
                    </v-toolbar>
                    <v-divider></v-divider>
                    <v-card-text>
                        <v-list-item two-line>
                            <v-list-item-content>
                                <v-list-item-title>
                                    Qualification
                                </v-list-item-title>
                                <v-list-item-subtitle>
                                    {{ item.qualification }}
                                </v-list-item-subtitle>
                            </v-list-item-content>
                        </v-list-item>
                        <v-list-item two-line>
                            <v-list-item-content>
                                <v-list-item-title>
                                    School
                                </v-list-item-title>
                                <v-list-item-subtitle>
                                    {{ item.school }}
                                </v-list-item-subtitle>
                            </v-list-item-content>
                        </v-list-item>
                        <v-list-item two-line>
                            <v-list-item-content>
                                <v-list-item-title>
                                    Subject
                                </v-list-item-title>
                                <v-list-item-subtitle>
                                    {{ item.subject }}
                                </v-list-item-subtitle>
                            </v-list-item-content>
                        </v-list-item>
                    </v-card-text>
                </v-card>

            </v-timeline-item>
        </v-timeline>
    </div>
</template>

<script>
export default {
    data: () => ({
        items: [

            {
                start: '2013',
                end: '2022',
                school: 'Surin Technical College',
                subject: 'Electrotype',
                qualification: 'High Vocational Certificate'
            },
            {
                start: '2010',
                end: '2013',
                school: 'Sawai Witthayakarn',
                subject: 'Science-Mathematics',
                qualification: 'High School Education'
            },
        ],
    }),
}
</script>
<style scoped></style>