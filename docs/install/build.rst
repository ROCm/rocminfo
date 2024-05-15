

Build ROCmInfo
*****************

Use the standard cmake build procedure to build rocminfo. The location of ROCm root (parent directory containing ROCM headers and libraries) must be provided
as a cmake argument using the standard CMAKE_PREFIX_PATH cmake variable.

After cloning the rocminfo git repo, please make sure to do a git-fetch --tags to get the tags residing on the repo. These tags are used for versioning.

For example,

.. code-block::

    $ git fetch --tags origin
    
    Building from the CMakeLists.txt directory might look like this:
    
    mkdir -p build
    
    cd build
    
    cmake -DCMAKE_PREFIX_PATH=/opt/rocm ..
    
    make
    
    cd ..

Upon a successful build, the binary, rocminfo, and the python script, rocm_agent_enumerator, will be in the `build` folder.
