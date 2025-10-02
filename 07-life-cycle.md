## lifecycle
### creation
- prepare the component
- run AJAX calls, initialize some variables
- no access to the template (DOM)
### mounting
- initialize an external library (`new Lib()`)
  - that needs access to the template
- has access to the template (DOM)
### update
- debug
- update data/view
### unmounting
- remove what is not necessary (`Lib.destroy()`)
  - to free memory
