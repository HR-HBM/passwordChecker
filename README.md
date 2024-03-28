# passwordChecker

this javascript file uses Express.js to check if a password entered by a user via a form matched a predefined password. depending on the outome of the validation, the user is either redirected to another website or the current page is reloaded.

the folloowing middleware was created to check the password entered by the user.

function passwordCheck(req, res, next) {
    console.log(req.body.password);
    const password = req.body.password;
    req.userIsAuthorised = password === "ILoveProgramming";
    next();
}

