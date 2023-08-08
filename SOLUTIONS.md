#Live link: https://react-test-cases.netlify.app/

# Solutions

## Task

In this exercise, you'll create two more test scenarios to verify the form submission works as expected:
1. User is able to submit the form if the score is lower than 5 and additional feedback is provided
##### Solution
    const rangeInput = screen.getByLabelText(/Score:/);
    fireEvent.change(rangeInput, {target: {value: score}});

    const textArea = screen.getByLabelText(/Comments:/);
    fireEvent.change(textArea, {target: {value: comment}});

    const submitButton = screen.getByRole('button');
    fireEvent.click(submitButton);
2. User is able to submit the form if the score is higher than 5, without additional feedback
#### Solution
    const rangeInput = screen.getByLabelText(/Score:/);
    fireEvent.change(rangeInput, {target: {value: score}});

    const submitButton = screen.getByRole('button');
    fireEvent.click(submitButton)
    
