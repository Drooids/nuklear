# Changelog

- 2016/08/29 (1.11) - Removed some internal complexity and overly complex code
                        handling panel padding and panel border.
- 2016/08/29 (1.10) - Added additional height parameter to `nk_combobox_xxx`
- 2016/08/29 (1.10) - Fixed drawing bug in dynamic popups
- 2016/08/29 (1.10) - Added experimental mouse scrolling to popups, menus and comboboxes
- 2016/08/26 (1.10) - Added window name string prepresentation to account for
                        hash collisions. Currently limited to NK_WINDOW_MAX_NAME
                        which in term can be redefined if not big enough.
- 2016/08/26 (1.10) - Added stacks for temporary style/UI changes in code
- 2016/08/25 (1.10) - Changed `nk_input_is_key_pressed` and 'nk_input_is_key_released'
                        to account for key press and release happening in one frame.
- 2016/08/25 (1.10) - Added additional nk_edit flag to directly jump to the end on activate
- 2016/08/17 (1.096)- Removed invalid check for value zero in nk_propertyx
- 2016/08/16 (1.095)- Fixed ROM mode for deeper levels of popup windows parents.
- 2016/08/15 (1.094)- Editbox are now still active if enter was pressed with flag
                        `NK_EDIT_SIG_ENTER`. Main reasoning is to be able to keep
                        typing after commiting.
- 2016/08/15 (1.094)- Removed redundant code
- 2016/08/15 (1.094)- Fixed negative numbers in `nk_strtoi` and remove unused variable
- 2016/08/15 (1.093)- Fixed `NK_WINDOW_BACKGROUND` flag behavior to select a background
                        window only as selected by hovering and not by clicking.
- 2016/08/14 (1.092)- Fixed a bug in font atlas which caused wrong loading
                        of glyphes for font with multiple ranges.
- 2016/08/12 (1.091)- Added additional function to check if window is currently
                        hidden and therefore not visible.
- 2016/08/12 (1.091)- nk_window_is_closed now queries the correct flag `NK_WINDOW_CLOSED`
                        instead of the old flag `NK_WINDOW_HIDDEN`
- 2016/08/09 (1.09) - Added additional double version to nk_property and changed
                        the underlying implementation to not cast to float and instead
                        work directly on the given values.
- 2016/08/09 (1.08) - Added additional define to overwrite library internal
                        floating pointer number to string conversion for additional
                        precision.
- 2016/08/09 (1.08) - Added additional define to overwrite library internal
                        string to floating point number conversion for additional
                        precision.
- 2016/08/08 (1.072)- Fixed compiling error without define NK_INCLUDE_FIXED_TYPE
- 2016/08/08 (1.071)- Fixed possible floating point error inside `nk_widget` leading
                        to wrong wiget width calculation which results in widgets falsly
                        becomming tagged as not inside window and cannot be accessed.
- 2016/08/08 (1.07) - Nuklear now differentiates between hiding a window (NK_WINDOW_HIDDEN) and
                        closing a window (NK_WINDOW_CLOSED). A window can be hidden/shown
                        by using `nk_window_show` and closed by either clicking the close
                        icon in a window or by calling `nk_window_close`. Only closed
                        windows get removed at the end of the frame while hidden windows
                        remain.
- 2016/08/08 (1.06) - Added `nk_edit_string_zero_terminated` as a second option to
                        `nk_edit_string` which takes, edits and outputs a '\0' terminated string.
- 2016/08/08 (1.054)- Fixed scrollbar auto hiding behavior
- 2016/08/08 (1.053)- Fixed wrong panel padding selection in `nk_layout_widget_space`
- 2016/08/07 (1.052)- Fixed old bug in dynamic immediate mode layout API, calculating
                        wrong item spacing and panel width.
- 2016/08/07 (1.051)- Hopefully finally fixed combobox popup drawing bug
- 2016/08/07 (1.05) - Split varargs away from NK_INCLUDE_STANDARD_IO into own
                        define NK_INCLUDE_STANDARD_VARARGS to allow more fine
                        grained controlled over library includes.
- 2016/08/06 (1.045)- Changed memset calls to NK_MEMSET
- 2016/08/04 (1.044)- Fixed fast window scaling behavior
- 2016/08/04 (1.043)- Fixed window scaling, movement bug which appears if you
                        move/scale a window and another window is behind it.
                        If you are fast enough then the window behind gets activated
                        and the operation is blocked. I now require activating
                        by hovering only if mouse is not pressed.
- 2016/08/04 (1.042)- Fixed changing fonts
- 2016/08/03 (1.041)- Fixed `NK_WINDOW_BACKGROUND` behavior
- 2016/08/03 (1.04) - Added color parameter to `nk_draw_image`
- 2016/08/03 (1.04) - Added additional window padding style attributes for
                        sub windows (combo, menu, ...)
- 2016/08/03 (1.04) - Added functions to show/hide software cursor
- 2016/08/03 (1.04) - Added `NK_WINDOW_BACKGROUND` flag to force a window
                        to be always in the background of the screen
- 2016/08/03 (1.032)- Removed invalid assert macro for NK_RGB color picker
- 2016/08/01 (1.031)- Added helper macros into header include guard
- 2016/07/29 (1.03) - Moved the window/table pool into the header part to
                        simplify memory management by removing the need to
                        allocate the pool.
- 2016/07/29 (1.03) - Added auto scrollbar hiding window flag which if enabled
                        will hide the window scrollbar after NK_SCROLLBAR_HIDING_TIMEOUT
                        seconds without window interaction. To make it work
                        you have to also set a delta time inside the `nk_context`.
- 2016/07/25 (1.02) - Fixed small panel and panel border drawing bugs
- 2016/07/15 (1.01) - Added software cursor to `nk_style` and `nk_context`
- 2016/07/15 (1.01) - Added const correctness to `nk_buffer_push' data argument
- 2016/07/15 (1.01) - Removed internal font baking API and simplified
                        font atlas memory management by converting pointer
                        arrays for fonts and font configurations to lists.
- 2016/07/15 (1.01) - Changed button API to use context dependend button
                        behavior instead of passing it for every function call.

