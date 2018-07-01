<head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1">

    <title>Bootstrap 4, from LayoutIt!</title>

    <meta name="description" content="Source code generated using layoutit.com">
    <meta name="author" content="LayoutIt!">

    <link href="css/bootstrap.min.css" rel="stylesheet">
    <link href="css/style.css" rel="stylesheet">
</head>
<template>
    <div id='add-prm'>
        <h3>Payment Request Memo</h3>
        <form>
            <table>
                <tr>
                    <td>
                        <div class="form-group">
                            <label>Prm No:</label>
				            <input type="text" v-model.lazy="prmNo" required/>
			            </div>
                    </td>
                    <td>
                        <div class="form-group">
                            <label>Prm Date:</label>
				            <input type="date" v-model.lazy="prmDate" required/>
			            </div>
                    </td>
                </tr>
                <tr>
                    <td>
                        <div class="form-group">
                            <label>From:</label>
				            <input type="text" v-model.lazy="from" required/>
			            </div>
                    </td>
                    <td>
                        <div class="form-group">
				            <label>Pay To:</label>
				            <input type="text" v-model.lazy="payTo" required/>
			            </div>
                    </td>
                </tr>
                <tr>
                    <td>
                        <div class="form-group">
				            <label>Mode of payment:</label>
				            <select v-model="paymentMode">
                                <option v-for="paymentMode in paymentModes">{{paymentMode}}</option>
                            </select>
			            </div>
                    </td>
                    <td>
                        <div class="form-group">
                            <label>Date:</label>
				            <input type="date" v-model.lazy="receivedDate" required/>
			            </div>
                    </td>
                </tr>
                <tr>
                    <td>
                        <div class="form-group">
				            <label>Cost Centre:</label>
				            <select v-model="costCenter">
                                <option v-for="costCenter in costCenters">{{costCenter}}</option>
                            </select>
			            </div>
                    </td>
                    <td>
                        <div class="form-group">
				            <label>Location:</label>
                            <select v-model="location">
                                <option v-for="location in locations">{{location}}</option>
                            </select>
			            </div>
                    </td>
                </tr>
                <tr>
                    <td>
                        <div class="form-group">
				            <label>Po No:</label>
				            <input type="text" v-model.lazy="poNumber" required/>
			            </div>
                    </td>
                    <td>
                        <div class="form-group">
				        <label>Prepared By:</label>
				        <input type="text" v-model.lazy="preparedBy" required/>
			            </div>
                    </td>
                </tr>
                <tr>
                    <td>
                        <div class="form-group">
                            <label>Checked By:</label>
                            <input type="text" v-model.lazy="checkedBy" required/>
                        </div>
                    </td>
                    <td>
                        <div class="form-group">
                            <label>Approved By Tier1:</label>
                            <input type="text" v-model.lazy="approvedByTier1" required/>
                        </div>
                    </td>
                </tr>
                <tr>
                    <td>
                        <div class="form-group">
                            <label>Approved By Tier2:</label>
                            <input type="text" v-model.lazy="approvedByTier2" required/>
                        </div>
                    </td>
                    <td>
                        <div class="form-group">
                            <label>Approved By Tier3:</label>
                            <input type="text" v-model.lazy="approvedByTier3" required/>
                        </div>
                    </td>
                </tr>
                <tr>
                    <td>
                        <div class="form-group">
                            <label>Received By:</label>
                            <input type="text" v-model.lazy="receivedBy" required/>
                        </div>
                    </td>
                </tr>
            </table>
            <table class="table">
                <thead>
					<tr>
						<th>
							Particulars of Expenses
						</th>
						<th>
							Bill No.
						</th>
						<th>
							Bill Date
						</th>
						<th>
							Bill Amount
						</th>
						<th>
							Approved
						</th>
						<th>
							Gross Amount To be Paid
						</th>
						<th>
							Remarks
						</th>
					</tr>
				</thead>
                <tbody>
                    <tr>
                        <td>
                            <select v-model="accountDetails.expenseParticulars">
                                <option v-for="expenseParticular in expenseParticulars">{{expenseParticular}}</option>
                            </select>
                        </td>
                        <td>
                            <input type="text" v-model.lazy="accountDetails.billNo" required/>
                        </td>
                        <td>
                            <input type="date" v-model.lazy="accountDetails.billDate" required/>
                        </td>
                        <td>
                            <input type="text" v-model.lazy="accountDetails.billAmount" required/>
                        </td>
                        <td>
                            <input type="text" v-model.lazy="accountDetails.approvedAmount" required/>
                        </td>
                        <td>
                            <input type="text" v-model.lazy="accountDetails.grossAmount" required/>
                        </td>
                        <td>
                            <input type="text" v-model.lazy="accountDetails.remarks" required/>
                        </td>
                    </tr>
                </tbody>
            </table>
            <button v-on:click.prevent="post">Add Prm</button>
        </form>
    </div>
</template>

<script>

export default {
  
  data () {
    return {
        prmNo: "",
        receivedDate: "",
        prmDate: "",
        from: "",
        payTo: "",
        paymentMode: "",
        paymentModes: ['Wire Transfer','Cheque'],
        costCenter: "",
        costCenters: ['ABC', 'DEF', 'XYZ'],
        location: "",
        locations: ['Paradigm'],
        poNumber: "",
        preparedBy: "",
        checkedBy: "",
        approvedByTier1: "",
        approvedByTier2: "",
        approvedByTier3: "",
        receivedBy: "",
        accountDetails:{
            expenseParticulars: "",
            billNo: "",
            billDate: "",
            billAmount: "",
            approvedAmount: "",
            grossAmount: "",
            remarks: ""
        },
        expenseParticulars: ['Training & Recruitment','Travel & Entertainment','Postage & Courier','Telephone & Mobile']
    }
  },
  methods:{
      post: function(){
          console.log(this.prmNo);
          console.log(this.receivedDate);
          console.log(this.prmDate);
          console.log(this.from);
          console.log(this.payTo);
          console.log(this.paymentMode);
          console.log(this.costCenter);
          console.log(this.location);
          console.log(this.poNumber);
          console.log(this.preparedBy);
          console.log(this.checkedBy);
          console.log(this.approvedByTier1);
          console.log(this.approvedByTier2);
          console.log(this.approvedByTier3);
          console.log(this.receivedBy);
          console.log(this.accountDetails.expenseParticulars);
          console.log(this.accountDetails.billNo);
          console.log(this.accountDetails.billDate);
          console.log(this.accountDetails.billAmount);
          console.log(this.accountDetails.approvedAmount);
          console.log(this.accountDetails.grossAmount);
          console.log(this.accountDetails.remarks);

            //post call
            this.$http.post('http://localhost:3000/prm',{
                prmNo: this.prmNo,
                receivedDate: this.receivedDate,
                prmDate: this.prmDate,
                from: this.from,
                payTo: this.payTo,
                paymentMode: this.paymentMode,
                costCenter:this.costCenter,
                location: this.location,
                poNumber: this.poNumber,
                preparedBy: this.preparedBy,
                checkedBy: this.checkedBy,
                approvedByTier1: this.approvedByTier1,
                approvedByTier2: this.approvedByTier2,
                approvedByTier3: this.approvedByTier3,
                receivedBy: this.receivedBy,
                accountDetails: this.accountDetails
            }).then(function(data){
                console.log('data inserted');
                console.log(data);
            });
            
            /*this.$http.post('http://localhost:3000/todo',{
                item: 'test1'
            }).then(function(data){
                console.log('done');
            });
            this.$http.post('http://localhost:3000/test',{
                prmNo: 'test'
            }).then(function(data){
                console.log('test done');
            });*/
      }
  }
}
</script>

<style>
    
</style>
