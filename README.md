# Validations

Lightweight input validation for PHP.

## Usage

validator.add_fields('name', 'email', 'email_confirmation');

Validations::method('post');

Validations::validate('username', ['non_empty', 'is_alphanum']);
Validations::validate('password', ['non_empty', 'length_gte 8']);
Validations::validate('password_confirm', ['non_empty', 'confirms password']);
Validations::validate('day', ['non_empty', 'numeric', 'in 1 31']);
Validations::validate('month', ['non_empty', 'numeric', 'in 1 12']);
Validations::validate('year', ['non_empty', 'numeric', 'in 1900 2100']);
Validations::validate('email', ['non_empty', 'is_email']);
Validations::validate('email_confirm', ['non_empty', 'confirms email']);
Validations::validate('accept_terms', ['non_empty', 'is_true']);

if(Validations::is_valid){
  $input = Validations::get_input;
  // Action logic
}
else{
  $input = Validatoins::get_errors();
  // Action logic
}
