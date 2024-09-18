<template>
    <div>
        <v-timeline dense>
            <v-timeline-item v-for="(item, i) in items" :key="i" color="success">
                <v-card>
                    <v-card-text >
                      <v-list-item two-line>
                            <v-list-item-content>
                                <v-list-item-title>
                                    {{item.en}}
                                </v-list-item-title>
                                <v-list-item-subtitle>
                                    {{item.th}}
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
                en: 'Lathe',
                th: '(เครื่องกลึง)',
            },
                     {
                en: 'Milling Machine',
                th: '(เครื่องมิลลิ่ง)',
            },
                     {
                en: 'Nat Pump Machine',
                th: '(เครื่องปั๊มน๊อต)',
            },
        ],
    }),
}
</script>
<style scoped></style>
