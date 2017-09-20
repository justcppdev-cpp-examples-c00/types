# Типы в С++
```
- integral_type [](std::is_integral, порядковой тип)
	- bool
	- char
	- char16_t
	- char32_t
	- wchar_t
	- short
	- int
	- long
	- long long

- floating_type [](std::is_floating_point, вещественный тип)
	- float
	- double
	- long double

- arithmetic_type [](std::is_arithmetic, арифмитический тип)
	- integral_type
	- floating_type

- fundamental_type [](std::is_fundamental, фундаментальный тип)
	- arithmetic_type
	- void
	- nullptr_t

- compound_type [](std::is_compound, составной тип)
	- !fundamental_type

- enum_type [](std::is_enum, тип-перечесление)
	- enum

- scalar_type [](std::is_scalar, скалярный тип)
	- arithmetic_type
	- enum_type
	- pointer_type
	- member_pointer
	- nullptr_t

- union_type [](std::is_union, тип-объединение)
	- union
	
- class_type [](std::is_class, тип-класс)
	- class
	- struct

- object_type [](std::is_object, тип-объект)
	- scalar_type
	- array_type
	- union_type
	- class_type

- array_type [](std::is_array, тип-массив)
	- object_type[]

- pointer_type [](std::is_pointer, тип-указтель)
	- object_type *
	- void *
	- return_type(*)(param_type)

- member_object_pointer_type [](std::is_member_object_pointer, тип-указатель-на-атрибут-класса)
	- object_type(class_type::*)
	
- member_function_pointer_type [](std::is_member_fuction_pointer, тип-указатель на-метод-класса)
	- return_type(class_type::*)(param_type)

- member_pointer_type [](std::is_member_pointer, тип-указатель-на-член-класса)
	- member_object_pointer_type
	- member_function_pointer_type

- lvalue_reference_type [](std::is_lvalue_reference)
	- object_type &

- rvalue_reference_type [](std::is_rvalue_reference)
	- object_type &&

- reference_type [](std::is_reference, ссылочный тип)
	- lvalue_reference_type
	- rvalue_reference_type

- return_type [](возвращаемый тип)
	- scalar_type
	- union_type
	- class_type
	- reference_type
	- pointer_type
	- member_pointer_type

- param_type [](тип-параметр)
	- object_type
	- void
	- reference_type
	
- function_type [](std::is_function, тип-функция)
	- return_type(param_type)

1 == sizeof(char) <= sizeof(short) <= sizeof(int) <= sizeof(long) <= sizeof(long long)
```
