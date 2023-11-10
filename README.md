# learning_analytics_dashboard
Learning Analytics Dashboard for teachers of primary and secondary school in German. It's part of my bachelor thesis in collaboration with "Future Applications and Media" of the Fraunhofer Institute for Open Communication Systems (FOKUS).
The foundations of this project is a local moodle setup combined with an LRS for xAPI data. The moodle includes a quiz for the students to decide which information they want to submit for the dashboard. This is the focus of the thesis: data sovereignty. That means that only allowed submitted data is used for the dashboard.

This project includes 3 jupyter notebooks:
1. dashboard LRS xAPI: This notebook handles the xAPI data from 'moodle-dashboard.son' to delete unauthorized data. The new data is stored in 'new_statements.json'.
2. dashboard moodle database: This notebook handles data from the moodle database, deletes unauthorized data and creates the learning analytics dashboard. Since the moodle database is local it is important to use the code that fetches the dataset from 'moodle_dataset.csv', 'df_souv.csv' and 'quiz.csv'. It's marked red.
3. generate_extended_dataset: This notebook uses 'example_data_set.csv' to generate the bigger dataset 'extension_for_moodle_data.csv' that fits in with the dataset from the second dashboard. It is used there to showcase the dashboard wich synthetical data.
