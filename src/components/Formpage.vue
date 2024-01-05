

<template>
    <div>
        <div class="card">
            <!-- First Division -->
            <div class="division">
                <h3>Form Elements</h3>
                <div class="mb-3 row">

                    <label class="InputLabel">Input Field</label>
                    <br />
                    <div class="col-sm-10">
                        <input type="text" readonly value="Input Placeholder">
                    </div>
                </div>
                <div class="mb-3 row">
                    <label class="InputLabel">Input Field Focus</label>
                    <br />
                    <div class="col-sm-10">
                        <input type="text" class="Inputfocus">

                    </div>
                    <div class="mb-3 row">
                        <label class="InputLabel">Input Field Disabled</label>
                        <br />
                        <div class="col-sm-10">
                            <input type="text" disabled readonly class="disableInput" value="Input Placeholder">
                        </div>
                    </div>

                    <div class="mb-3 row">
                        <label class="InputLabel">Input Field Error</label>
                        <br />
                        <div class="col-sm-10">
                            <input type="text" value="Input Placeholder" class="errorInput">

                        </div>
                    </div>
                    <div class="mb-3 row">
                        <label class="InputLabel"> Custom Input Field </label>
                        <br />
                        <div class="col-sm-10">
                            <input type="text" value="Input Placeholder">
                        </div>
                    </div>

                    <div class="mb-3 row">
                        <label class="InputLabel"> Input Number Field </label>
                        <br />
                        <div class="col-sm-10">
                            <input type="number" value="Input Placeholder">
                        </div>
                    </div>
                    <div class="mb-3 row">
                        <label class="InputLabel"> Text Area </label>
                        <br />
                        <div class="col-sm-10">
                            <textarea name="type here" id="textarea" cols="30" rows="6" style="margin-left:50px"></textarea>
                        </div>
                    </div>

                </div>

            </div>

            <div class="division2">
                <br />
                <div class="mb-3 row">
                    <label class="InputLabel"> Dropdown with Search</label>

                    <div class="col-sm-10">
                        <select class="form-select" v-model="selectedOption">
                            <option v-for="option in filterOptions" :value="option.value" :key="option.value">{{ option.label }}</option>
                          </select>
                    </div>
                </div>
                <br />
                <br />
                <br />
                <br />
                <br />
                <br />
                <div class="mb-3 row">
                    <label class="InputLabel"> Date Select</label>

                    <div class="col-sm-10">
                        <input type="date" />
                    </div>
                </div>
                <br />
                <br />
                <br />
                <br />
                <br />
               
                <br />
                <div class="mb-3 row">
                    <label class="InputLabel3"> ToolTips</label>

                    <div class="col-sm-10">
                        <div class="tooltip"> ToolTips
                            <span class="tooltiptext">$234,435,647,982.23 USD plan 85,215 lines</span>
                        </div>

                    </div>
                </div>
            </div>

            <div class="division3">
                <div class="mb-3 row">
                    <label class="InputLabel"> Toasts</label>

                    <div class="container">

                        <button type="button" 
                        class="custom-toast  
                               success-toast" @click="showSuccessToast"> 
                    Submit 
                  </button>
                  <br/>
                  <button type="button" 
                  class="custom-toast  
                         danger-toast"  @click="showDangerToast"> 
              Failed 
            </button> 
            <br/>
          <button type="button" 
                  class="custom-toast  
                         info-toast" @click="showInfoToast"> 
              Information 
            </button> 
            <br/>
          <button type="button" 
                  class="custom-toast  
                         warning-toast" @click="showWarningToast"> 
              Warning 
            </button> 
            <br/>

          
         
                    </div>
                    <div v-if="showingToast" :class="['toast', `toast-${currentToastType}`]">
                        <div class="toast-content-wrapper">
                          <div class="toast-icon" v-html="icon[currentToastType]"></div>
                          <div class="toast-message">{{ currentToastMessage }}</div>
                          <div class="toast-progress" :style="{ animationDuration: durationInSeconds + 's' }"></div>
                        </div>
                      </div>

                </div>
                <div class="mb-3 row">
                    <label class="InputLabel"> Chips</label>

                    <div class="col-sm-10">
                        <div class="chip">
                            <img src="https://upload.wikimedia.org/wikipedia/en/thumb/4/41/Flag_of_India.svg/1200px-Flag_of_India.svg.png" alt="Person" width="96" height="96">
                           India
                          </div>
                          <div class="chip">
                            <img src="https://cdn.britannica.com/79/4479-050-6EF87027/flag-Stars-and-Stripes-May-1-1795.jpg" alt="Person" width="96" height="96">
                         USA
                          </div>
    
                          <div class="chip">
                            <img src="https://media.istockphoto.com/id/468505976/photo/chinese-flag.jpg?s=612x612&w=0&k=20&c=vQ_QcveuMYWHKihYiR9Fig-EXIZvY3OIwSRuzKi44_Y=" alt="Person" width="96" height="96">
                         China
                          </div>
                          <div class="chip">
                            <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/19/Flag_of_Ghana.svg/255px-Flag_of_Ghana.svg.png" alt="Person" width="96" height="96">
                         Ghana
                          </div>
                    </div>
                    <br/>
                    <br/>
                  <b>  Toggle </b>
                    <br/>
                    <label class="switch"> 
                        <input type="checkbox">
                        <span class="slider round"></span>
                      </label>
                      <label class="switch">
                        <input type="checkbox" class="togg">
                        <span class="slider round"></span>
                      </label>

                      <br/>
                      <br/>
                   <label>Bike</label>
                      <input type="checkbox" id="vehicle1" name="vehicle1" value="Bike">   <br/>
                      <label>Car</label>
                      <input type="checkbox" id="vehicle2" name="vehicle2" value="Car">
                   
                      <p>Radio Button:</p>
                       <input type="radio" id="html" name="fav_language" value="HTML" class="radio">
                       <input type="radio" id="css" name="fav_language" value="CSS" class="radio">

                       <input type="radio" id="javascript" name="fav_language" value="JavaScript" class="radio">




                      
                </div>
            
            </div>
        </div>
    </div>
</template>

<script>

export default {
    name: 'FormPage',

    data(){
        return{
            value: '',
            icon: {
        success: '<span class="material-symbols-outlined">task_alt</span>',
        danger: '<span class="material-symbols-outlined">error</span>',
        warning: '<span class="material-symbols-outlined">warning</span>',
        info: '<span class="material-symbols-outlined">info</span>',
      },
      selectedOption: null, 
      filterOptions: [
        { value: null, label: 'Open this select menu' },
        { value: '1', label: 'One' },
        { value: '2', label: 'Two' },
        { value: '3', label: 'Three' }
    ],
      showingToast: false,
      toastType: '',
      message: '',
      duration: 5000,
        }

    },

    methods: {
    showToast(message = 'Sample Message', toastType = 'info', duration = 5000) {
      if (!Object.keys(this.icon).includes(toastType)) {
        toastType = 'info';
      }
      this.message = message;
      this.toastType = toastType;
      this.duration = duration;

      this.showingToast = true;
      setTimeout(() => {
        this.showingToast = false;
      }, duration);
    },
    showSuccessToast() {
      this.showToast('Article Submitted Successfully', 'success', 5000);
    },
    showInfoToast() {
      this.showToast('Do POTD and Earn Coins', 'info', 5000);
    },
    showDangerToast() {
      this.showToast('Failed unexpected error', 'danger', 5000);
    },
    showWarningToast() {
      this.showToast('!warning! server error', 'warning', 5000);
    },
  },
};
</script>

<style scoped>

.card {
    max-width: 1500px; 
    margin: 0 auto; 
    padding: 20px; 
    border: 1px solid #ccc;
    border-radius: 8px;
    display: flex;
    justify-content: space-between; 
  }

  .division {
    flex: 1; 
    margin: 0 10px; 
    padding: 15px;
    border: 1px solid #eee;
    border-radius: 5px;
  }

  .division2{
    flex: 4; 
    margin: 0 10px; 
    padding: 15px;
    border: 1px solid #eee;
    border-radius: 5px;
  }

  .division3{
    flex: 4; 
    margin: 0 10px; 
    padding: 15px;
    border: 1px solid #eee;
    border-radius: 5px;
  }

  input {
    width: 200px;
    height: 30px;
    margin-bottom: 20px;
    margin-left: 50px;
    margin-top: 10px;
    color: gray;
    font-family: 'Times New Roman', Times, serif;

}
.disableInput{
    width: 200px;
    height: 30px;
    margin-bottom: 20px;
    margin-left: 50px;
    margin-top: 10px;
    color: gray;
    font-family: 'Times New Roman', Times, serif;
}
.InputLabel{

    margin-left: 50px;
    font-weight: 600;
    margin-bottom: 5px;
    font-family: 'Times New Roman', Times, serif;
}

.InputLabel3{
    margin-left: 50px;
    font-weight: 600;
    margin-bottom: 5px;
    font-family: 'Times New Roman', Times, serif;
    margin-top:50px
}

.errorInput {
    border: 1px solid red; 

}

.form-select{
    width: 200px;
    height: 30px;
    font-family: 'Times New Roman', Times, serif;
    margin-top:20px;
    margin-left:50px

}

.tooltip {
    position: relative;
    display: inline-block;
 margin-left: 50px;
  }

  /* Tooltip text */
  .tooltip .tooltiptext {
    visibility: hidden;
    width: 120px;
    background-color: rgb(248, 246, 246);
    color:gray;
    text-align: center;
    padding: 5px 0;
    border-radius: 6px;

    position: absolute;
    z-index: 1;
  }

  .tooltip:hover .tooltiptext {
    visibility: visible;
  }

  .toast{
    border:1px solid rgb(246, 240, 240) ;
    background-color: #ffffff;

  }

   
.toast-buttons { 
    max-width: 700px; 
    display: flex; 
    flex-wrap: wrap; 
    justify-content: center; 
    gap: 15px; 
    margin: 2em auto; 
} 
  
.toast-row { 
    display: flex; 
    justify-content: center; 
    margin: 1em 0; 
    padding: 1rem; 
    flex-wrap: wrap; 
} 
  
button.custom-toast { 
    padding: 0.5rem 1rem; 
    border: none; 
    color: #fff; 
    font-weight: 200; 
    border-radius: 5px; 
   
    cursor: pointer; 
    width: 80px; 
    margin: 0.5em; 
    transition: filter 0.2s ease-in-out, 
        transform 0.3s ease-in-out; 
    display: flex; 
    justify-content: center; 
    align-items: center; 
    font-size: 12px; 
    background-color: transparent; 
    outline: none; 
    background: #3498db; 
    color: #fff; 
} 
  
button.custom-toast:hover { 
    filter: brightness(0.9); 
} 
  
button.success-toast { 
    background-color: #2ecc71; 
} 
  
button.danger-toast { 
    background-color: #e74c3c; 
} 
  
button.info-toast { 
    background-color: #3498db; 
} 
  
button.warning-toast { 
    background-color: #f1c40f; 
} 
  
h1 { 
    color: green; 
} 
  
.toast { 
    position: fixed; 
    top: 25px; 
    right: 25px; 
    max-width: 300px; 
    background: #fff; 
    padding: 0.5rem; 
    border-radius: 4px; 
    box-shadow: -1px 1px 10px
        rgba(0, 0, 0, 0.3); 
    z-index: 1023; 
    animation: slideInRight 0.3s 
            ease-in-out forwards, 
        fadeOut 0.5s ease-in-out 
            forwards 3s; 
    transform: translateX(110%); 
} 
  
.toast.closing { 
    animation: slideOutRight 0.5s 
        ease-in-out forwards; 
} 
  
.toast-progress { 
    position: absolute; 
    display: block; 
    bottom: 0; 
    left: 0; 
    height: 4px; 
    width: 100%; 
    background: #b7b7b7; 
    animation: toastProgress 3s 
        ease-in-out forwards; 
} 
  
.toast-content-wrapper { 
    display: flex; 
    justify-content: space-between; 
    align-items: center; 
} 
  
.toast-icon { 
    padding: 0.35rem 0.5rem; 
    font-size: 1.5rem; 
} 
  
.toast-message { 
    flex: 1; 
    font-size: 0.9rem; 
    color: #000000; 
    padding: 0.5rem; 
} 
  
.toast.toast-success { 
    background: #95eab8; 
} 
  
.toast.toast-success .toast-progress { 
    background-color: #2ecc71; 
} 
  
.toast.toast-danger { 
    background: #efaca5; 
} 
  
.toast.toast-danger .toast-progress { 
    background-color: #e74c3c; 
} 
  
.toast.toast-info { 
    background: #bddaed; 
} 
  
.toast.toast-info .toast-progress { 
    background-color: #3498db; 
} 
  
.toast.toast-warning { 
    background: #ead994; 
} 
  
.toast.toast-warning .toast-progress { 
    background-color: #f1c40f; 
} 
  
@keyframes slideInRight { 
    0% { 
        transform: translateX(110%); 
    } 
  
    75% { 
        transform: translateX(-10%); 
    } 
  
    100% { 
        transform: translateX(0%); 
    } 
} 
  
@keyframes slideOutRight { 
    0% { 
        transform: translateX(0%); 
    } 
  
    25% { 
        transform: translateX(-10%); 
    } 
  
    100% { 
        transform: translateX(110%); 
    } 
} 
  
@keyframes fadeOut { 
    0% { 
        opacity: 1; 
    } 
  
    100% { 
        opacity: 0; 
    } 
} 
  
@keyframes toastProgress { 
    0% { 
        width: 100%; 
    } 
  
    100% { 
        width: 0%; 
    } 
}
.chip {
    display: inline-block;
    padding: 0 25px;
    height: 50px;
    font-size: 16px;
    line-height: 50px;
    border-radius: 25px;
    background-color: #f1f1f1;
  }
  
  .chip img {
    float: left;
    margin: 0 10px 0 -25px;
    height: 50px;
    width: 50px;
    border-radius: 50%;
  }

  .switch {
    position: relative;
    display: inline-block;
    width: 50px;
    height: 30px;
  }
  
  .switch input { 
    opacity: 0;
    width: 0;
    height: 0;
  }
  
  .slider {
    position: absolute;
    cursor: pointer;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background-color: #ccc;
    -webkit-transition: .4s;
    transition: .4s;
  }
  
  .slider:before {
    position: absolute;
    content: "";
    height: 23px;
    width: 25px;
    left: 4px;
    bottom: 4px;
    background-color: white;
    -webkit-transition: .4s;
    transition: .4s;
  }
  
  input:checked + .slider {
    background-color: #2196F3;
  }
  
  input:focus + .slider {
    box-shadow: 0 0 1px #2196F3;
  }
  
  input:checked + .slider:before {
    -webkit-transform: translateX(26px);
    -ms-transform: translateX(26px);
    transform: translateX(26px);
  }
  
  /* Rounded sliders */
  .slider.round {
    border-radius: 34px;
  }
  
  .slider.round:before {
    border-radius: 50%;
  }
  .togg{
 padding-right: 10px;
  }

  #vehicle1{
    height: 20px;
    width:20px
  }
  #vehicle2{
    height: 20px;
    width:20px
    
  }

  .radio{
    width:15px
  }
</style>
