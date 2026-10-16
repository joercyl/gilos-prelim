
ruby jane
5:44 PM (0 minutes ago)
to me

<template>
  <div class="page">
    <header class="hero">
      <div class="container">
        <p class="eyebrow">Admissions</p>
        <h1>Apply, Estimate, Enroll</h1>
        <p class="lead">
          Take the next step toward a purposeful future. Explore our programs, prepare your documents,
          and connect with the Admissions Office for application guidance.
        </p>
        <button class="primary-btn">Start Your Application</button>
      </div>
    </header>

    <main class="container main">

      <!-- Requirements -->
      <section class="card">
        <h2>Admission Requirements</h2>

        <div class="requirements-grid">

          <div>
            <h3>Admission Process</h3>
            <ul>
              <li>Choose a program and complete the application form.</li>
              <li>Submit the required academic and identity documents.</li>
              <li>Complete any program-specific assessment or interview.</li>
              <li>Confirm your enrollment with the Admissions Office.</li>
            </ul>
          </div>

          <div>
            <h3>Requirements</h3>
            <ul>
              <li>Completed application form.</li>
              <li>Latest school record or transcript.</li>
              <li>Proof of identity and recent ID photos.</li>
              <li>Additional documents requested for your chosen program.</li>
            </ul>
          </div>

          <div>
            <h3>Programs Offered</h3>
            <ul>
              <li>BS Computer Science</li>
              <li>BS Information Technology</li>
              <li>BS Nursing</li>
              <li>BA Communication</li>
            </ul>
          </div>

        </div>
      </section>

      <!-- Tuition Calculator -->
      <section class="card">
        <h2>Tuition Fee Calculator</h2>

        <p class="muted">
          Select your program and units to estimate your fees for one semester.
          This is an estimate only - final assessment is issued by the Registrar's Office.
        </p>

        <div class="form-grid">

          <label class="field">
            <span>Program</span>
            <select v-model="program">
              <option>BS Computer Science</option>
              <option>BS Information Technology</option>
              <option>BS Business Administration</option>
              <option>BS Education</option>
              <option>BS Nursing</option>
            </select>
          </label>

          <label class="field">
            <span>Year Level</span>
            <select v-model="year">
              <option>1st Year</option>
              <option>2nd Year</option>
              <option>3rd Year</option>
              <option>4th Year</option>
            </select>
          </label>

          <label class="field">
            <span>Units this semester: {{ units }}</span>
            <input
              v-model="units"
              type="range"
              min="12"
              max="27"
              value="21"
            />

            <div class="range-labels">
              <span>12</span>
              <span>27</span>
            </div>
          </label>

        </div>

        <div class="payment-terms">
          <span>Payment Terms</span>

          <div class="button-group">
            <button
              type="button"
              class="pill"
              :class="{ active: payment === 'Full' }"
              @click="payment = 'Full'"
            >
              Full Payment
            </button>

            <button
              type="button"
              class="pill"
              :class="{ active: payment === '3' }"
              @click="payment = '3'"
            >
              3 Installments
            </button>

            <button
              type="button"
              class="pill"
              :class="{ active: payment === '5' }"
              @click="payment = '5'"
            >
              5 Installments
            </button>
          </div>
        </div>

        <!-- Fees -->
        <div class="table-wrap">
          <table>
            <thead>
              <tr>
                <th>Schedule of Fees</th>
                <th class="align-right">Amount</th>
              </tr>
            </thead>

            <tbody>
              <tr>
                <td>Tuition Fee ({{ units }} units x ₱650)</td>
                <td class="align-right">₱{{ (units * 650).toLocaleString() }}</td>
              </tr>

              <tr>
                <td>Laboratory Fee ({{ units }} units x ₱150)</td>
                <td class="align-right">₱{{ (units * 150).toLocaleString() }}</td>
              </tr>

              <tr>
                <td>Miscellaneous Fee (8% of tuition)</td>
                <td class="align-right">₱1,092</td>
              </tr>

              <tr class="muted-row">
                <td>Registration Fee</td>
                <td class="align-right">₱750</td>
              </tr>

              <tr class="muted-row">
                <td>Library Fee</td>
                <td class="align-right">₱500</td>
              </tr>

              <tr class="muted-row">
                <td>Athletic Fee</td>
                <td class="align-right">₱350</td>
              </tr>

              <tr class="muted-row">
                <td>Medical & Dental Fee</td>
                <td class="align-right">₱400</td>
              </tr>

              <tr class="muted-row">
                <td>Guidance & Testing Fee</td>
                <td class="align-right">₱300</td>
              </tr>

              <tr class="muted-row">
                <td>ID & Insurance Fee</td>
                <td class="align-right">₱450</td>
              </tr>

              <tr class="muted-row">
                <td>Student Organization Fee</td>
                <td class="align-right">₱250</td>
              </tr>
            </tbody>

            <tfoot>
              <tr class="total-row">
                <td>Total Assessment (1st Year)</td>
                <td class="align-right">₱20,892</td>
              </tr>
            </tfoot>
          </table>
        </div>

        <p class="fine-print">
          * Rates shown are sample figures for demonstration purposes.
          Replace with your institution's actual schedule of fees.
        </p>
      </section>

      <!-- CTA -->
      <section class="cta">
        <button class="primary-btn">
          Start Your Application
        </button>
      </section>

    </main>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const program = ref('BS Computer Science')
const year = ref('1st Year')
const units = ref(21)
const payment = ref('Full')
</script>

<style scoped>
* {
  box-sizing: border-box;
}

.page {
  min-height: 100vh;
  background: #fbf8f1;
  color: #352b27;
  font-family: Arial, Helvetica, sans-serif;
}

.container {
  max-width: 960px;
  margin: 0 auto;
  padding: 0 24px;
}

/* Hero */
.hero {
  background: #780e1c;
  color: #fff8e9;
  padding: 48px 0;
  border-bottom: 1px solid #c8943d;
}

.eyebrow {
  font-size: 13px;
  text-transform: uppercase;
  letter-spacing: 0.05em;
  color: #e8c77d;
  margin: 0 0 8px;
}

.hero h1 {
  font-size: 32px;
  margin: 0 0 12px;
}

.lead {
  max-width: 640px;
  color: #f4e9d5;
  line-height: 1.6;
}

/* Main */
.main {
  padding: 36px 24px;
}

.card {
  padding: 24px 0 30px;
  border-bottom: 1px solid #e6dcc9;
}

.card h2 {
  color: #780e1c;
  font-size: 22px;
  margin: 0 0 20px;
}

.muted {
  color: #64748b;
}

/* Requirements */
.requirements-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 32px;
}

.requirements-grid h3 {
  font-size: 16px;
  color: #333333;
}

.requirements-grid ul {
  padding-left: 20px;
  color: #475569;
  line-height: 1.8;
}

/* Form */
.form-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 16px;
  margin-top: 20px;
}

.field {
  display: block;
  font-size: 14px;
}

.field span {
  display: block;
  font-weight: 600;
  margin-bottom: 6px;
}

select {
  width: 100%;
  padding: 10px 12px;
  border: 1px solid #d9c8aa;
  border-radius: 2px;
  background: white;
  font-size: 14px;
}

input[type="range"] {
  width: 100%;
  margin-top: 12px;
}

.range-labels {
  display: flex;
  justify-content: space-between;
  font-size: 12px;
  color: #94a3b8;
  margin-top: 4px;
}

/* Payment */
.payment-terms {
  margin: 24px 0;
}

.payment-terms > span {
  display: block;
  font-weight: 600;
  margin-bottom: 8px;
}

.button-group {
  display: flex;
  gap: 8px;
  flex-wrap: wrap;
}

.pill {
  padding: 8px 14px;
  border-radius: 2px;
  font-size: 14px;
  border: 1px solid #cbd5e1;
  background: white;
  color: #475569;
  cursor: pointer;
}

.pill.active {
  background: #780e1c;
  border-color: #780e1c;
  color: white;
}

/* Table */
.table-wrap {
  border: 1px solid #e6dcc9;
  border-radius: 2px;
  overflow: hidden;
}

table {
  width: 100%;
  border-collapse: collapse;
  font-size: 14px;
}

thead {
  background: #f2eadb;
  color: #780e1c;
  text-transform: uppercase;
  font-size: 12px;
}

th,
td {
  padding: 10px 16px;
  text-align: left;
}

tbody tr {
  border-top: 1px solid #f1f5f9;
}

.align-right {
  text-align: right;
}

.muted-row {
  color: #64748b;
}

.total-row {
  background: #f8f4ec;
  border-top: 1px solid #e6dcc9;
  font-weight: 700;
}

.fine-print {
  font-size: 12px;
  color: #94a3b8;
  margin: 16px 0 0;
}

/* Button */
.primary-btn {
  background: #780e1c;
  color: white;
  border: none;
  padding: 12px 24px;
  border-radius: 2px;
  font-size: 15px;
  font-weight: 600;
  cursor: pointer;
}

.primary-btn:hover {
  background: #5d0914;
}

.cta {
  text-align: center;
  padding: 24px 0 40px;
}

/* Responsive */
@media (max-width: 640px) {
  .requirements-grid {
    grid-template-columns: 1fr;
  }

  .form-grid {
    grid-template-columns: 1fr;
  }

  .hero h1 {
    font-size: 30px;
  }

  .container {
    padding: 0 16px;
  }

  th,
  td {
    padding: 10px;
  }
}
</style>
