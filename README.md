### Building and Running the Application
###### Run the following commands in terminal
```
wget https://github.com/glfw/glfw/releases/download/3.3.3/glfw-3.3.3.zip \
  && unzip glfw-3.3.3.zip \
  && cd glfw-3.3.3 \
  && mkdir build \
  && cd build \
  && cmake -DBUILD_SHARED_LIBS=ON .. \
  && make -j4 \
  && sudo make install \
  && cd ../../ \
  && rm -rf glfw*
```

```
wget https://github.com/g-truc/glm/releases/download/0.9.8.5/glm-0.9.8.5.zip \
  && unzip glm-0.9.8.5.zip \
  && sudo cp -R glm/glm /usr/local/include/ \
  && rm -rf glm*
```

```
wget https://github.com/nigels-com/glew/releases/download/glew-2.2.0/glew-2.2.0.zip \
  && unzip glew-2.2.0.zip \
  && cd glew-2.2.0 \
  && make -j4 \
  && sudo make install GLEW_DEST=/usr/local \
  && cd .. \
  && rm -rf glew*
```

#### Initializing the data will automatically happen when you run the program for the first time

### Build and Run

```
mkdir build
cd build
cmake ..
make -j4
cd ..
```
```
./build/rubiksCube
```

### Keys

Twist the faces of the cube using these keys: `U`, `L`, `F`, `R`, `B`, and `D`
for up, left, front, right, back, and down twists, respectively.  Hold `SHIFT`
for prime (counter-clockwise) moves, or `ALT` for double (180-degree) twists.

Rotate the entire cube using the arrow keys: `UP`, `DOWN`, `LEFT`, and `RIGHT`
for X and Y rotations.  Press `Z` for a Z rotation (hold `SHIFT` for prime).

For slice moves, use `M`, `E`, and `S` for the respective slices.

Rapidly solve a scrambled cube using Thistlethwaite's algorithm by pressing
`F1`.

To solve a scrambled cube optimally using the Korf algorithm, press `F2`.

Apply a 100-move scramble by pressing `F5`.
