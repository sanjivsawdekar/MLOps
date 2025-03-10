# Docker Setup

Maker sure that virtualization is enabled on your machine.

<img src="./media/image1.png" style="width:5.22in;height:4.63in" />

Download VirtualBox. Windows 10 Home Edition requires VirtualBox.
Windows 10 Professional does not.

<https://www.virtualbox.org/wiki/Downloads>

Download Docker Toolbox for Windows 10 Home.

Launch docker from desktop shortcut & try below commands.

**\$docker version**

<img src="./media/image2.png" style="width:5.625in;height:5.23958in" />

**\$docker run hello-world**

Downloads the hello-world image only first time if not available
locally.

<img src="./media/image3.png"
style="width:6.26806in;height:1.13889in" />

**\$docker run redis**

<img src="./media/image4.png"
style="width:6.26806in;height:1.96667in" />

<img src="./media/image5.png"
style="width:6.26806in;height:3.52569in" />

<img src="./media/image6.png"
style="width:6.26806in;height:3.52569in" />

<img src="./media/image7.png"
style="width:6.26806in;height:3.52569in" />

<img src="./media/image8.png"
style="width:6.26806in;height:1.16597in" />

Changing start-up command – Above example runs default command that
comes with image.

<img src="./media/image9.png"
style="width:6.26806in;height:0.68264in" />

<img src="./media/image10.png"
style="width:6.26806in;height:2.11528in" />

`Ctrl+C` to exit from above command.

<img src="./media/image11.png" style="width:2.43in;height:1.84in" />

Display currently active containers. They need to be stopped explicitly.
Hello-world just displays the message & exits, hence it is not visible
in below list.

<img src="./media/image12.png"
style="width:6.26806in;height:0.56458in" />

To display all containers including the exit ones –

<img src="./media/image13.png"
style="width:6.26806in;height:1.04028in" />

**\$docker stop \<CONTAINER ID\>** 🡨 to stop the specific container

Validate that the contains is stopped by command docker ps.

<img src="./media/image14.png" style="width:5in;height:0.25in" />

<img src="./media/image15.png"
style="width:6.26806in;height:4.35556in" />

**-a** option is used to attach CLI to container so that the output is
redirected to CLI.

To see inside the running container –

<img src="./media/image16.png"
style="width:6.26806in;height:1.30139in" />

**\$docker kill \<ID\>** 🡨to forcefully kill the container when the
container is not responding

To see inside the running container using the container shell –

<img src="./media/image17.png"
style="width:6.26806in;height:1.3375in" />

`Ctrl+D` to exit from the shell of container. **-i** (interactive) to pass
input to container shell from CLI. **-t** (terminal) is for formatting
the output of container shell. You can combine them as **-it**
(interactive terminal).

**Dockerfile** – text file used for building your own custom image from
other existing image.

<img src="./media/image18.png"
style="width:6.26806in;height:3.52569in" />

<img src="./media/image19.png"
style="width:6.26806in;height:3.52569in" />

<img src="./media/image20.png"
style="width:6.26806in;height:3.52569in" />

Create Dockerfile & add commands & build the docker with command docker
build .

<img src="./media/image21.png"
style="width:6.26806in;height:3.52569in" />

Once build completes, run the docker.

<img src="./media/image22.png"
style="width:6.26806in;height:3.52569in" />

<img src="./media/image23.png"
style="width:6.26806in;height:3.52569in" />

Every step modifies file system snapshot & removes intermediate
container & takes snapshot of new file system.

<img src="./media/image24.png"
style="width:6.26806in;height:3.52569in" />

<img src="./media/image25.png"
style="width:6.26806in;height:3.52569in" />

<img src="./media/image26.png"
style="width:6.26806in;height:1.19722in" />

<img src="./media/image27.png"
style="width:6.26806in;height:0.84722in" />

Commit the docker & set the start-up command –

<img src="./media/image28.png"
style="width:6.26806in;height:0.53472in" />

Run the docker with partial string –

<img src="./media/image29.png"
style="width:6.26806in;height:0.90972in" />
