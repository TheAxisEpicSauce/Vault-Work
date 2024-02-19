### Fields
int: id
int: passenger_id
int: insurance_id
string: policy_holder_type
int: policy_holder_id
int: reservation_id
bool: active
bool: latest
date_time: registration_period
date_time: registration_date_time
date_time: reservation_start_period
date_time: reservation_start_date_time
string: function_type
float: insurance_value
float: insured_sum
float: policy_fee
float: insurance_tax
text: extensions


#### tasks
- when calculating insurance register the insurance
- when confirmin the reservation check active insurance registration
- 1 if none are active -> set active
- 2 if has active and same period but new values -> update the current registrations values
- 3 if has active of previous period and new values -> set new registration as active with function type mutation

#tpi 