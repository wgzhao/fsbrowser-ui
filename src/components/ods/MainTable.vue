<template>
    <!-- ODS 主表信息 ODS采集主表配置-->
    <!-- <v-sheet class="mx-auto"> -->
        <v-card flat title="ODS采集主表配置">
        <v-form fast-fail @submit.prevent>
            <v-container>
                <v-row  no-gutters>
                    <v-col cols="12" md="3" class="m-0">
                        <v-text-field v-model="d.sysName" label="源系统"></v-text-field>
                    </v-col>
                    <v-col cols="12" md="3">
                        <v-text-field v-model="d.souFilter" label="源筛选"></v-text-field>
                    </v-col>
                    <v-col cols="12" md="3">
                        <v-text-field v-model="d.souOwner" label="源用户"></v-text-field>
                    </v-col>
                    <v-col cols="12" md="3">
                        <v-text-field v-model="d.souTablename" label="源表名"></v-text-field>
                    </v-col>
                </v-row>

                <v-row  no-gutters>
                    <v-col cols="12" md="3">
                        <v-text-field v-model="d.destTablename" label="目标表"></v-text-field>
                    </v-col>
                    <v-col cols="12" md="3">
                        <v-text-field v-model="d.destPartKind" label="入库规则"></v-text-field>
                    </v-col>
                    <v-col cols="12" md="3">
                        <v-text-field v-model="d.flag" label="状态"></v-text-field>
                    </v-col>
                    <v-col cols="12" md="3">
                        <v-text-field v-model="d.retryCnt" label="剩余次数"></v-text-field>
                    </v-col>
                </v-row>

                <v-row  no-gutters>
                    <v-col cols="12" md="3">
                        <v-text-field v-model="d.paramSou" label="参数组"></v-text-field>
                    </v-col>
                    <v-col cols="12" md="3">
                        <v-text-field v-model="d.bpreview" label="预发布"></v-text-field>
                    </v-col>
                    <v-col cols="12" md="3">
                        <v-text-field v-model="d.bcreate" label="是否建表"></v-text-field>
                    </v-col>
                    <v-col cols="12" md="3">
                        <v-text-field v-model="d.bupdate" label="是否更新"></v-text-field>
                    </v-col>
                </v-row>


                <v-row  no-gutters>
                    <v-col cols="12" md="3">
                        <v-text-field v-model="d.realtimeInterval" label="实时间隔"></v-text-field>
                    </v-col>
                    <v-col cols="12" md="3">
                        <v-text-field v-model="d.realtimeTaskgroup" label="实时任务组"></v-text-field>
                    </v-col>
                    <v-col cols="12" md="3">
                        <v-text-field v-model="d.realtimeSouOwner" label="实时源用户"></v-text-field>
                    </v-col>
                    <v-col cols="12" md="3">
                        <v-text-field v-model="d.realtimeSouFilter" label="实时筛选条件"></v-text-field>
                    </v-col>
                </v-row>

                <v-row  no-gutters>
                    <v-col cols="12" md="3">
                        <v-text-field v-model="d.realtimeFixed" label="实时定点"></v-text-field>
                    </v-col>
                    <v-col cols="12" md="3">
                        <v-text-field v-model="d.etlKind" label="采集模式"></v-text-field>
                    </v-col>
                    <v-col cols="12" md="3">
                        <v-text-field v-model="d.realtimeIntervalRange" label="实时间隔范围"></v-text-field>
                    </v-col>
                    <v-col cols="12" md="3">
                        <v-text-field v-model="d.souSplit" label="源表分片字段"></v-text-field>
                    </v-col>
                </v-row>

                <v-row  no-gutters>
                    <v-col cols="12" md="3">
                        <v-text-field v-model="d.afterRetryPntype" label="盘后重采计划"></v-text-field>
                    </v-col>
                    <v-col cols="12" md="3">
                        <v-text-field v-model="d.afterRetryFixed" label="盘后重采时间"></v-text-field>
                    </v-col>
                    <v-col cols="12" md="3">
                        <v-text-field v-model="d.startTime" label="开始时间"></v-text-field>
                    </v-col>
                    <v-col cols="12" md="3">
                        <v-text-field v-model="d.endTime" label="结束时间"></v-text-field>
                    </v-col>
                </v-row>

                <v-row  no-gutters>
                    <v-col cols="12" md="3">
                        <v-text-field v-model="d.runtime" label="运行耗时"></v-text-field>
                    </v-col>
                    <v-col cols="12" md="3">
                        <v-text-field v-model="d.tid" label="编号"></v-text-field>
                    </v-col>
                    <v-col cols="12" md="3">
                        <v-text-field v-model="d.runtimeAdd" label="运行耗时手工"></v-text-field>
                    </v-col>
                    <v-col cols="12" md="3">
                        <v-text-field v-model="d.remark" label="备注"></v-text-field>
                    </v-col>
                </v-row>
            </v-container>
        </v-form>
        </v-card>
    <!-- </v-sheet> -->
</template>
<script>

export default {
    name: 'tableInfo',
    props: ['d'],
}
</script>
<style>
.v-input .v-field  {
    font-size: 0.9rem;
}
</style>