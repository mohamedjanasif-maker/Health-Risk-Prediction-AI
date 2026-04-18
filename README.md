نظام ذكي يعتمد على الذكاء الاصطناعي للتنبؤ بالمخاطر الصحية باستخدام العلامات الحيوية. يتميز المشروع بتقديم **تفسير منطقي (Explainable AI)** لكل قرار يتخذه الموديل.

 (Project Structure)
- **/model**: يحتوي على ملف الـ `.pkl` الخاص بنموذج Random Forest والـ Scaler.
- **/src**: يحتوي على كود الربط (Logic) المسؤول عن إخراج النتائج بصيغة **JSON** للـ API.
- **/notebooks**: يحتوي على ملفات التدريب ورسومات التحليل (SHAP & Correlation).

 (Tech Stack)
- **Model:** Random Forest Classifier (Accuracy: 99.85%).
- **XAI Layer:** SHAP Framework لتفسير النتائج.
- **Data Handling:** Pandas, Numpy, Scikit-learn.
- **Communication:** JSON API Response format.
(JSON Output)
{
  "status": "Risk",
  "explanation": "Risk detected: contributing factors are Blood Pressure, Oxygen Saturation",
  "risk_factors": [
    {
      "feature": "Blood Pressure",
      "value": 140.0,
      "impact": 0.528
    },
    {
      "feature": "Oxygen Saturation",
      "value": 100.0,
      "impact": 0.004
    }
  ]
}
