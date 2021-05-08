<template>
    <div>
        <!-- nav bar -->
        <b-navbar toggleable type="dark" variant="info">
            <b-navbar-brand href="#" style="font-weight:bold;">급여명세서</b-navbar-brand>

            <b-navbar-toggle target="navbar-toggle-collapse">
            <template #outline-primary="{ expanded }">
                <b-icon v-if="expanded" icon="chevron-bar-up"></b-icon>
                <b-icon v-else icon="chevron-bar-down"></b-icon>
            </template>
            </b-navbar-toggle>

            <b-collapse id="navbar-toggle-collapse" is-nav>
            <b-navbar-nav class="ml-auto">
                <b-nav-item href="#">지급내역관리</b-nav-item>
                <b-nav-item href="#">경영성과금</b-nav-item>
                <b-nav-item href="#">성과연봉</b-nav-item>
                <b-nav-item href="#">특별격려금</b-nav-item>
                <b-nav-item href="#">연차수당</b-nav-item>
                <b-nav-item href="#">연말정산</b-nav-item>
                <b-nav-item href="#">연봉통지서</b-nav-item>
                <b-nav-item href="#">퇴직금적립현황</b-nav-item>
                <b-nav-item href="#">사내근로복지기금</b-nav-item>
                <b-nav-item href="#">사우회대부금</b-nav-item>
                <b-nav-item href="#">직원아파트대부금</b-nav-item>
                <b-nav-item href="#">국내학자금보조</b-nav-item>
                <b-nav-item href="#">경조금지급내역</b-nav-item>
                <b-nav-item href="#">우리사주</b-nav-item>
                <b-nav-item href="#">국민연금</b-nav-item>
                <b-nav-item href="#">건강보험</b-nav-item>
                <b-nav-item href="#">단체보험</b-nav-item>
            </b-navbar-nav>
            </b-collapse>
        </b-navbar>

        <!-- table -->

            <b-table
            :striped="striped"
            :bordered="bordered"
            :borderless="borderless"
            :outlined="outlined"
            :small="small"
            :hover="hover"
            :dark="dark"
            :fixed="fixed"
            :foot-clone="footClone"
            :no-border-collapse="noCollapse"
            :fields="fields"
            :head-variant="headVariant"
            :table-variant="tableVariant"
            ></b-table>
   
        <b-form inline>
            <b-form-select
            id="inline-form-custom-select-pref"
            class="mb-2 mr-sm-2 mb-sm-0"
            :options="[{ text: '2021.04 급여', value: null }, '2021.04 경영성과금', '2021.04 명절상여금']"
            :value="null"
            style="width:50%;margin-left:5px" 
            ></b-form-select>
            <b-button variant="info"
            style="margin-left:10px;margin-bottom:6px;">조회</b-button>
        </b-form>
        <!-- table -->
         <b-table-simple hover small caption-top responsive>
            <colgroup><col><col></colgroup>
            <colgroup><col><col><col></colgroup>
            <colgroup><col><col></colgroup>
            <b-thead head-variant="dark">
            <b-tr>
                <b-th colspan="2" style="text-align:center;">지급내역</b-th>
                <b-th colspan="2" style="text-align:center;">공제내역</b-th>
            </b-tr>
            </b-thead>
            <b-tbody>
            <b-tr>
                <b-th class="text-right contentgy">기본연봉</b-th>
                <b-td class="contentgy" style="text-align:right;">2,941,500</b-td>
                <b-th class="text-right contentgy">소득세</b-th>
                <b-td class="contentgy" style="text-align:right;">269,700</b-td>
            </b-tr>
            <b-tr>
                <b-th class="text-right contentgy">개인평가급</b-th>
                <b-td class="contentgy" style="text-align:right;">507,221</b-td>
                <b-th class="text-right contentgy">지방소득세</b-th>
                <b-td class="contentgy" style="text-align:right;">26,970</b-td>
            </b-tr>
            <b-tr>
                <b-th class="text-right contentgy">기타지급3</b-th>
                <b-td class="contentgy" style="text-align:right;">1,000,000</b-td>
                <b-th class="text-right contentgy">국민연금</b-th>
                <b-td class="contentgy" style="text-align:right;">174,100</b-td>
            </b-tr>
            <b-tr>
                <b-th class="text-right contentgy">식대(중식)</b-th>
                <b-td class="contentgy" style="text-align:right;">99,000</b-td>
                <b-th class="text-right contentgy">건강보험</b-th>
                <b-td class="contentgy" style="text-align:right;">176,780</b-td>
            </b-tr>
            <b-tr>
                <b-th class="text-right contentgy"></b-th>
                <b-td></b-td>
                <b-th class="text-right contentgy">건강보험정산추징</b-th>
                <b-td class="contentgy" style="text-align:right;">174,770</b-td>
            </b-tr>
            <b-tr>
                <b-th class="text-right contentgy"></b-th>
                <b-td class="contentgy"></b-td>
                <b-th class="text-right contentgy">장기요양보험</b-th>
                <b-td class="contentgy" style="text-align:right;">20,370</b-td>
            </b-tr>
            <b-tr>
                <b-th class="text-right contentgy"></b-th>
                <b-td></b-td>
                <b-th class="text-right contentgy">고용보험</b-th>
                <b-td class="contentgy" style="text-align:right;">35,580</b-td>
            </b-tr>
            <b-tr>
                <b-th class="text-right contentgy"></b-th>
                <b-td></b-td>
                <b-th class="text-right contentgy">건강보험정산추징</b-th>
                <b-td class="contentgy" style="text-align:right;">174,770</b-td>
            </b-tr>
            <b-tr>
                <b-th class="text-right contentgy"></b-th>
                <b-td></b-td>
                <b-th class="text-right contentgy">사내복지기금대부금</b-th>
                <b-td class="contentgy" style="text-align:right;">478,128</b-td>
            </b-tr>
            <b-tr>
                <b-th class="text-right contentgy"></b-th>
                <b-td></b-td>
                <b-th class="text-right contentgy">기타공제</b-th>
                <b-td class="contentgy" style="text-align:right;">1,000,000</b-td>
            </b-tr>
            <b-tr>
                <b-th class="text-right contentgy"></b-th>
                <b-td></b-td>
                <b-th class="text-right contentgy">중식비(사용)</b-th>
                <b-td class="contentgy" style="text-align:right;">23,000</b-td>
            </b-tr>
            <b-tr>
                <b-th class="text-right contentgy"></b-th>
                <b-td></b-td>
                <b-th class="text-right contentgy" >기부금</b-th>
                <b-td class="contentgy" style="text-align:right;">5,000</b-td>
            </b-tr>
            </b-tbody>
            <b-tfoot>
            <b-tr>
                <b-td colspan="2" variant="secondary" class="text-right">
                
                </b-td>
                <b-td colspan="2" variant="secondary" class="text-right"
                style="font-size:smaller;">
                실지급액: <b>2,163,323</b>
                </b-td>
            </b-tr>
            </b-tfoot>
            <b-tfoot>
            <b-tr>
                <b-td colspan="2" variant="secondary" class="text-right"
                style="font-size:smaller;">
                총지급액: <b>4,547,721</b>
                </b-td>
                <b-td colspan="2" variant="secondary" class="text-right"
                style="font-size:smaller;">
                공제총액: <b>2,384,398</b>
                </b-td>
            </b-tr>
            </b-tfoot>
        </b-table-simple>
    </div>
    
</template>
<style>
    .contentgy {
        font-size: smaller;
    }
</style>
<script>
export default {
    name : 'Read',
    data() {
        return {
            fields: ['백홍차', '부장', 'P1/2.0', '-'],
        
            bordered: true,
            tableVariant: '',
             items: [
                { age: 40, first_name: 'Dickerson', last_name: 'Macdonald' },
                { age: 21, first_name: 'Larsen', last_name: 'Shaw' },
                { age: 89, first_name: 'Geneva', last_name: 'Wilson' },
                { age: 38, first_name: 'Jami', last_name: 'Carney' }
            ]
        }
    }
}
</script>