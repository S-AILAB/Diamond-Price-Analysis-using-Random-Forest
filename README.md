

<h1>💎 Diamond Price Prediction using Random Forest Regression</h1>

<p>This project explores how various diamond attributes — such as carat, cut, color, clarity, and physical dimensions — affect diamond prices. Using <strong>Random Forest Regression</strong>, the model predicts diamond prices with high accuracy by learning from these features.</p>

<h2>📌 Why This Matters</h2>
<p>Diamond pricing is complex and influenced by multiple interacting factors. An accurate predictive model helps jewelers, appraisers, and buyers estimate fair market prices efficiently and reliably.</p>

<h2>📁 Dataset Overview</h2>
<p>The dataset contains the following attributes:</p>
<ul>
  <li><strong>Carat:</strong> Weight of the diamond</li>
  <li><strong>Cut:</strong> Quality of the cut (Fair to Ideal)</li>
  <li><strong>Color:</strong> Color grading scale from J (worst) to D (best)</li>
  <li><strong>Clarity:</strong> Clarity grade (I1 to IF)</li>
  <li><strong>Dimensions:</strong> Length, Width, Depth (in mm)</li>
  <li><strong>Total Depth Percentage</strong> and <strong>Table Width</strong></li>
  <li><strong>Price:</strong> Target variable (in USD)</li>
</ul>

<h2>🛠️ Project Workflow</h2>

<h3>🔹 1. Data Cleaning & Preprocessing</h3>
<ul>
  <li>Removed duplicate entries (less than 1% of data).</li>
  <li>Handled outliers in numeric columns using IQR-based capping.</li>
  <li>Renamed columns for clarity.</li>
  <li>Checked for missing values (none found).</li>
  <li>Encoded categorical variables (<code>Cut</code>, <code>Color</code>, <code>Clarity</code>) with Label Encoding.</li>
  <li>Scaled numeric features using StandardScaler for normalization.</li>
</ul>

<h3>🔹 2. Exploratory Data Analysis (EDA)</h3>
<ul>
  <li>Visualized distributions of numeric features with histograms.</li>
  <li>Explored relationships between features and price using scatterplots.</li>
  <li>Analyzed categorical variables using countplots and bivariate plots.</li>
  <li>Generated correlation heatmaps to study feature interactions.</li>
</ul>

<h3>🔹 3. Model Building</h3>
<ul>
  <li>Split data into training and test sets (test size = 20 samples).</li>
  <li>Trained a baseline Random Forest Regressor model.</li>
  <li>Predicted diamond prices on test data.</li>
  <li>Evaluated performance with R-squared, RMSE, and MAE metrics.</li>
</ul>

<h3>🔹 4. Hyperparameter Tuning</h3>
<ul>
  <li>Used GridSearchCV for cross-validation and parameter optimization (n_estimators, max_depth, min_samples_split, max_features).</li>
  <li>Retrained the model with the best found parameters.</li>
  <li>Re-evaluated model performance on the test set.</li>
</ul>

<h2>📈 Key Results</h2>
<table border="1" cellpadding="8" cellspacing="0">
  <thead>
    <tr>
      <th>Metric</th>
      <th>Before Tuning</th>
      <th>After Tuning</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>R-squared</strong></td>
      <td>0.9906</td>
      <td>0.9926</td>
    </tr>
    <tr>
      <td><strong>RMSE</strong></td>
      <td>$358.98</td>
      <td>$316.72</td>
    </tr>
    <tr>
      <td><strong>MAE</strong></td>
      <td>$224.00</td>
      <td>$218.25</td>
    </tr>
  </tbody>
</table>

<h2>🔍 Interpretation</h2>
<p>The model explains over 99% of the variance in diamond prices. The average prediction errors (RMSE and MAE) around $220-$320 indicate the model predicts prices quite closely despite diamond valuation's inherent complexity.</p>

<h2>🚀 How to Use This Repository</h2>
<ol>
  <li>Clone or download this repository.</li>
  <li>Place the <code>diamonds.csv</code> dataset in the specified path or update the path in the code accordingly.</li>
  <li>Run the scripts or notebook to reproduce data cleaning, exploratory analysis, model training, tuning, and evaluation.</li>
  <li>Optionally, experiment with hyperparameters or try alternative regression models.</li>
</ol>

<h2>⚙️ Dependencies</h2>
<ul>
  <li>pandas</li>
  <li>numpy</li>
  <li>seaborn</li>
  <li>matplotlib</li>
  <li>scikit-learn</li>
</ul>

<p>Install required libraries via pip:</p>
<pre><code>pip install pandas numpy seaborn matplotlib scikit-learn</code></pre>

<h2>💡 Final Thoughts</h2>
<p>This project highlights the effectiveness of Random Forest regression for multi-feature price prediction. Future work could explore additional diamond-specific features, alternative models, or deployment for real-time price estimation.</p>

</body>
</html>
