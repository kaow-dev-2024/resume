<template>
    <div>
        <v-timeline dense>
            <v-timeline-item v-for="(item, i) in items" :key="i" color="success">
                <v-card>
                    <v-card-title >
                        {{ item.en }} {{ item.th }}
                    </v-card-title>

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
