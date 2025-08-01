# Template Repo for ML Project

This template repo will give you a good starting point for your second project. Besides the files used for creating a virtual environment, you will find a simple example of how to build a simple model in a python script. This is maybe the simplest way to do it. We train a simple model in the jupyter notebook, where we select only some features and do minimal cleaning. The output is then stored in simple python scripts.

The data used for this is: [coffee quality dataset](https://github.com/jldbc/coffee-quality-database).

In this README, you also find: 
* [How to set up your environment](#set-up-your-environment)
* [How to use this template repo](#usage)
* [How to set up a Kanban board on github](#set-up-a-kanban-board-on-github)
* [How to automatically format your Jupyter notebook according to Pep8](#pep-8-integration-for-jupyter-notebook)


---
## Set up your Environment



### **`macOS`** type the following commands : 



- For installing the virtual environment and the required package you can either follow the commands:

    ```BASH
    pyenv local 3.11.3
    python -m venv .venv
    source .venv/bin/activate
    pip install --upgrade pip
    pip install -r requirements.txt
    ```
Or ....
-  use the [Makefile](Makefile) and run `make setup` or install it manually with the following commands:

     ```BASH
    make setup
    ```
    After that active your environment by following commands:
    ```BASH
    source .venv/bin/activate
    ```

### **`WindowsOS`** type the following commands :

- Install the virtual environment and the required packages by following commands.

   For `PowerShell` CLI :

    ```PowerShell
    pyenv local 3.11.3
    python -m venv .venv
    .venv\Scripts\Activate.ps1
    pip install --upgrade pip
    pip install -r requirements.txt
    ```

    For `Git-bash` CLI :
  
    ```BASH
    pyenv local 3.11.3
    python -m venv .venv
    source .venv/Scripts/activate
    pip install --upgrade pip
    pip install -r requirements.txt
    ```

    **`Note:`**
    If you encounter an error when trying to run `pip install --upgrade pip`, try using the following command:
    ```Bash
    python.exe -m pip install --upgrade pip
    ```


---
## Usage

In order to train the model and store test data in the data folder and the model in models run:

**`Note`**: Make sure your environment is activated.

```bash
python example_files/train.py  
```

In order to test that predict works on a test set you created run:

```bash
python example_files/predict.py models/linear_regression_model.sav data/X_test.csv data/y_test.csv
```

### Limitations

Development libraries are part of the production environment, normally these would be separate as the production code should be as slim as possible.

---

## Set up a Kanban board on github

Go to ML-Project Template.

1. Click on "Use this Template" (Blue button)
![alt text](./images/step_1a_new.png)

2. Create new repository with relevant name, the owner should be your own account and **not** Spiced. 
![alt text](./images/step_2_new.png)

3. In your newly create repo, navigate to "Projects", and then click on "Link a project" (blue button). Normally you don't have created a project yet, so you can click the arrow navigation to create project on your profile. This project can be added at the end to your repository.
![alt text](./images/add_project_new.png)


4.  You will be guided to your profiles projects and it will be shown a create project window. Choose "board" view and **not** "table" view.
 ![alt text](./images/choose_board.png)
5. Now change the name of your board, to match that of your chosen ML project. Then click "Create project" blue button. Great you create Kanban Board
![alt text](./images/create_project_new.png)

6. Next, assign rights to all your team members by clicking on the 3 dots on the top right of the board, and then go to "Settings".
![alt text](./images/kanban_settings.png)


7. Next, click on "Manage Access". Add your team mates by Searching for their github handle in the search window.Change their Role from ‘Write’ to ‘Admin’. Click on the blue button “Invite” to add them. Repeat for all team members.
![alt text](./images/team_access_new.png
)

8. Next,go back to the kanban board and at the bottom  add action items with the relevant name e.g. “load data”, "get statistics", etc.
![alt text](./images/load_data_item.png
)


9. Convert added item to issue by clicking on the 3 dots on the particular added item.
![alt text](./images/convert_to_issue.png
)

10. Then select the repo you created  for the issue to be added. (Select the project repo example “my-project-name”)
![alt text](./images/select_repo.png
)

11. When in project repo, Go to issues, then go to milestones. 
![alt text](./images/to_milestones.png
)

12. Click on ”New milestone”.

13. Give the milestone a due date and description as per the example provided by the coaches. Add description of: 

    A) What needs to be completed to be done with the milestone

    B) The definition of done: what will your result look like when you have completed the milestone? (check the provided format)
![alt text](./images/new_milestone.png)

14. Now navigate to "issues".

15. Assign issues to milestones 
![alt text](./images/milestone_to_issue_new.png)

16. Give it assignees (people who will work on the task). 
![alt text](./images/milestone_to_someone.png)

### Optional: Add workflows

Workflows can help you keep your kanban board automatically on track. 

Select the project created in the steps above.  

Click on the 3 dots to the far right of the board (...)

Select workflow as the first option. 

Activate the ones you feel necessary to your project

Go back to your project repository (fraud detection))


---

## PEP 8 integration for Jupyter Notebook

This automatically formats all subsequent cells according to PEP 8 standards, once they are being run. Here is how to do it:

1. Go into your repo.
2. After activating your virtual environment, type into your terminal
```
pip install jupyter-black
```
3. Open your jupyter notebook and add at the beginning the following piece of code:
```
%load_ext jupyter_black
```
4. Run it.
5. Now any cells you run afterwards should be formatted according to PEP 8, as understood by Black.


