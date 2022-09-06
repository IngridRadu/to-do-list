# To do List React App
A React application wheret the user add all the tasks he has to do. The result is as a list of tasks which can be marked as completed, incompleted or delete it. Also the tasks can be sorted as complete, incomplete or all.

# Install 
npm install

## Run
npm start

# Quick Look 

App Component 
```
...
return (
    <div className="task-container">
      <div className="inputs-style">
        <input
          type="text"
          className="task-name"
          placeholder="add task..."
          value={value}
          onChange={(event) => setValue(event.target.value)}
        ></input>
        <FaPlus className="icon-input" onClick={() => addTask()} />

        <div className="dropdown-menu">
          <select
            name="option-items"
            id="option-items"
            className="list-items-open"
            onChange={(event) => setSelectedOption(event.target.value)}
          >
            <option key="all" value="all" className="item">
              All
            </option>
            <option key="completed" value="completed" className="item">
              Completed
            </option>
            <option key="incompleted" value="incompleted" className="item">
              Incompleted
            </option>
          </select>
        </div>
        {/* <RiArrowDropDownFill className="dropdown-arrow" /> */}
      </div>

      <ul className="list-style">
        {filterTasks().map((task) => {
          return (
            <Task
              task={task}
              key={task.id}
              incompleteTask={incompleteTask}
              confirmTask={confirmTask}
              deleteTask={deleteTask}
            />
          );
        })}
      </ul>
    </div>
  );
};

export default App;
```
