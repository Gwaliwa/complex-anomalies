# Werner–PSO real-case reproducibility package

This package uses the actual manuscript outputs currently available from the project, not synthetic or fake data.

It demonstrates the reproducible parts of the submitted workflow using the real files already generated for the Peak 4 case:

- detected anomaly peaks
- Werner batch solution table
- magnetic target-ranking table
- drillhole spatial-validation summary
- Euler solution table
- PSO result summary for the direct and decomposition-guided workflows
- actual generated manuscript figures

## Important

The exact numeric magnetic profile used inside the Streamlit session was not available as a CSV among the uploaded files. Therefore, this package does **not** reconstruct profile values from figure images. Instead, it includes:

1. the real available CSV outputs,
2. the real produced figures,
3. a small export script that saves the actual Streamlit session profile to CSV when you rerun the app.

This is the scientifically correct approach. Do not digitize the figure image and present it as original profile data.

## Run

```bash
pip install -r requirements.txt
python scripts/01_make_real_case_tables.py
python scripts/02_plot_real_case_summary.py
```

Outputs are written to `outputs/`.
