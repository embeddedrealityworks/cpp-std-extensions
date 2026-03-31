project(
    'stdx',
    'cpp',
    version: '0.1.0',
    license: 'BSL-1.0',
    meson_version: '>=1.1.0',
    default_options: ['cpp_std=c++23'],
)

fmt_sub = subproject('fmt')
fmt_dep = fmt_sub.get_variable('fmt_header_only_dep')
mp11_sub = subproject('mp11')
mp11_dep = mp11_sub.get_variable('mp11_dep')
concurrency_sub = subproject('cpp-baremetal-concurrency', default_options: ['simulate_freestanding=true'])
concurrency_dep = concurrency_sub.get_variable('concurrency_dep')

stdx_inc = include_directories('include')

stdx_dep = declare_dependency(
    include_directories: stdx_inc,
    dependencies: [fmt_dep, mp11_dep, concurrency_dep],
)

install_headers(
    'include/stdx/algorithm.hpp',
    'include/stdx/array.hpp',
    'include/stdx/atomic.hpp',
    'include/stdx/atomic_bitset.hpp',
    'include/stdx/bit.hpp',
    'include/stdx/bitset.hpp',
    'include/stdx/byterator.hpp',
    'include/stdx/cached.hpp',
    'include/stdx/call_by_need.hpp',
    'include/stdx/compiler.hpp',
    'include/stdx/concepts.hpp',
    'include/stdx/ct_conversions.hpp',
    'include/stdx/ct_format.hpp',
    'include/stdx/ct_string.hpp',
    'include/stdx/cx_map.hpp',
    'include/stdx/cx_multimap.hpp',
    'include/stdx/cx_queue.hpp',
    'include/stdx/cx_set.hpp',
    'include/stdx/cx_vector.hpp',
    'include/stdx/env.hpp',
    'include/stdx/for_each_n_args.hpp',
    'include/stdx/function_traits.hpp',
    'include/stdx/functional.hpp',
    'include/stdx/intrusive_forward_list.hpp',
    'include/stdx/intrusive_list.hpp',
    'include/stdx/iterator.hpp',
    'include/stdx/latched.hpp',
    'include/stdx/memory.hpp',
    'include/stdx/numeric.hpp',
    'include/stdx/optional.hpp',
    'include/stdx/panic.hpp',
    'include/stdx/pp_map.hpp',
    'include/stdx/priority.hpp',
    'include/stdx/ranges.hpp',
    'include/stdx/rollover.hpp',
    'include/stdx/span.hpp',
    'include/stdx/static_assert.hpp',
    'include/stdx/tuple.hpp',
    'include/stdx/tuple_algorithms.hpp',
    'include/stdx/tuple_destructure.hpp',
    'include/stdx/type_traits.hpp',
    'include/stdx/udls.hpp',
    'include/stdx/utility.hpp',
    subdir: 'stdx',
)

install_headers(
    'include/stdx/detail/bitset_common.hpp',
    'include/stdx/detail/fmt.hpp',
    'include/stdx/detail/freestanding.hpp',
    'include/stdx/detail/list_common.hpp',
    subdir: 'stdx/detail',
)
