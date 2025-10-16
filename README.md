import React from "react";
import ReactDOM from "react-dom/client";

// Functional component receiving 'name' as a prop
function Welcome({ name }) {
  return <h1>Welcome, {name}!</h1>;
}

// Main App component
function App() {
  const students = ["Deepak", "Nikhil", "Ananya"]; // Different student names

  return (
    <div>
      {students.map((student, index) => (
        <Welcome key={index} name={student} />
      ))}
    </div>
  );
}

// Render the App
const root = ReactDOM.createRoot(document.getElementById("root"));
root.render(<App />);
