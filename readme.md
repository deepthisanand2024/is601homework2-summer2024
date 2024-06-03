Install python using the Mac or Ubuntu instructions below. You will only do this step once for the course on your commputer. Mac needs Brew package manager to install Python and Ubuntu needs to just run the command:
sudo apt update -y
sudo apt install python3-pip
pip3 --version 
Install python virtual environment, so you can manage the virtual environment to issolate your dependences from the global version of python. You need to do this once for your computer, this is a global python package.
pip3 install virtualenv
note You should try the following to test your install with my project, after you have installed python and the virtual environment manager:

git clone git@github.com:kaw393939/git_python_testing_setup_homework.git
cd git_python_testing_setup_homework
source venv/bin/activate
pip3 install -r requirements.txt
pytest --pylint --cov
Now Make a project directory not inside my own project if you cloned mine. DO NOT CREATE A NEW REPO INSIDE OF THE ONE YOU CLONE FROM ME OR YOU WILL HAVE PROBLEMS, setup the virtual environment in the directory that you make for your projectand activate it. For more information see here. You need to do this for each new python project.
cd .. <-- goes up a directory to get out of the project  you cloned to test your install of python.  Make sure you do a pwd to see where your going to make your project from scratch.

mkdir myproject
cd myproject
virtualenv venv <- Makes a virtual environment in the venv directory (you can make this any directory but you will have to remember it to activate it correctlty)
source ./venv/bin/activate <- you should see (venv) in the terminal command line to indicate that the venv environment of your project is activated
Once the virtual environment is a active then install the python dependencies using pip:
pip3 install pytest pytest-pylint pytest-cov
Once you have the libraries installed you need to freeze the requiremnts and create your requirments.txt file. You need to do this so that the versions of the libaries / dependencies you use are saved, so that your project can be installed somewhere else.
pip3 freeze > requirements.txt
Note When someone copies / clones your repository they will install the specfic library / dependency requirements for your project using the command:

pip3 install -r requirments.txt
Once you have this done, you will need to create the "tests" and "calculator" folders and add the init.py file to each folder. You need a .gitignore with the same contents as mine, you need the .pylintrc file, and the pytest.ini file. You will need to put the same code that I have in those files.

Once you have the files made make sure you have the code that I have in my calculator folder's init.py file in yours and add the code for your test to the test_calculator.py file. Essentially, you should have the same files as what I have in this repository.

Run the tests:

pytest <-runs the tests without pylint or coverage
pytest --pylint <- Runs tests with pylint static code analysis
pytest --pylint --cov <-Runs tests, pylint, and coverage to check if you have all your code tested.

