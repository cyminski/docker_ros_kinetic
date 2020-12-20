FROM ubuntu:16.04

# install ROS
RUN apt-key adv --keyserver ha.pool.sks-keyservers.net --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros-latest.list

RUN apt-get update && apt-get install -y ros-kinetic-desktop
# setup entrypoint
COPY ./entrypoint.sh /
RUN chmod +x /entrypoint.sh

ENTRYPOINT ["/entrypoint.sh"]
CMD ["bash"]
