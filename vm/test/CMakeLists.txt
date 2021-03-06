cmake_minimum_required(VERSION 3.10)

project(vm_test C)

macro(add_run_test name)
  add_test(NAME "run_${name}" COMMAND bash "${CMAKE_CURRENT_SOURCE_DIR}/run_test.sh" "${runner_BINARY_DIR}/runner" "${CMAKE_CURRENT_SOURCE_DIR}/../../test_programs/${name}")
endmacro()

macro(add_run_stderr_test name)
  add_test(NAME "run_${name}" COMMAND bash "${CMAKE_CURRENT_SOURCE_DIR}/run_test_stderr.sh" "${runner_BINARY_DIR}/runner" "${CMAKE_CURRENT_SOURCE_DIR}/../../test_programs/${name}")
endmacro()

add_run_test(return_1)
add_run_test(multiply_21_and_2)
add_run_test(fact_recursive)
add_run_test(fact_iterative)
add_run_test(fact_iterative_34)
add_run_test(string_compare)
add_run_test(string_concat)
add_run_test(string_concat_compare)
add_run_test(index_array)
add_run_test(resize_array)
add_run_test(move_array)
add_run_test(fact_iterative_5000)
add_run_test(sum_iterative_10000000)
add_run_test(internal_function)
add_run_test(equals)
add_run_test(array_length)
add_run_test(force_marksweep)

add_run_test(prim_is_type)
add_run_test(prim_is_function_stream)
add_run_test(prim_math)
add_run_test(prim_display_number)
add_run_test(prim_display_float)
add_run_test(prim_display_singletons)
add_run_test(prim_display_string)
add_run_test(prim_display_more)
add_run_test(prim_pair)
add_run_test(prim_pair_arrays)
add_run_test(prim_list)
add_run_test(prim_list_arrays)
add_run_test(prim_map)
add_run_test(prim_map_arrays)
add_run_test(prim_map_primitive)
add_run_test(prim_equal)
add_run_test(prim_set_pair)
add_run_test(prim_set_pair_arrays)
add_run_test(prim_length)
add_run_test(prim_accumulate)
add_run_test(prim_accumulate_arrays)
add_run_test(prim_is_list)
add_run_test(prim_append)
add_run_test(prim_build_list)
add_run_test(prim_enum_list)
add_run_test(prim_filter)
add_run_test(prim_for_each)
add_run_test(prim_list_ref)
add_run_test(prim_member)
add_run_test(prim_remove)
add_run_test(prim_remove_all)
add_run_test(prim_reverse)
add_run_test(prim_stream)
add_run_test(prim_list_to_stream)
add_run_test(prim_build_stream)
add_run_test(prim_enum_stream)
add_run_test(prim_eval_stream)
add_run_test(prim_stream_to_list)
add_run_test(prim_stream_length)
add_run_test(prim_stream_for_each)
add_run_test(prim_integers_from)
add_run_test(prim_stream_append)
add_run_test(prim_stream_filter)
add_run_test(prim_stream_map)
add_run_test(prim_stream_member)
add_run_test(prim_stream_ref)
add_run_test(prim_stream_remove)
add_run_test(prim_stream_remove_all)
add_run_test(prim_stream_reverse)
add_run_test(prim_is_stream)

add_run_test(value_prim)
add_run_test(more_tail_calls)
add_run_test(more_arithmetic)
add_run_test(no_uninitialised_load)

add_run_test(prim_display)
add_run_test(prim_error)
add_run_test(hello_world)
