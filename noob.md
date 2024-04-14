sudo docker buildx build -f archdockerfile -t ansrepo:ans .
sudo docker run -it ansrepo:ans

The -it flag is a combination of two separate flags: -i and -t, which are
commonly used together when running Docker containers. Here's what each flag
does:

-i, or --interactive: Keeps STDIN open even if not attached. This flag allows
you to interact with the container's STDIN, enabling you to send input to the
running process within the container.

-t, or --tty: Allocates a pseudo-TTY. This flag allocates a pseudo-TTY
(teletypewriter) for the container, which simulates a terminal device. It's
often used to ensure that the output from the container's process is properly
formatted for your terminal.

When combined, -it is used to run a Docker container in interactive mode with a
pseudo-TTY, allowing you to interact with the container's process as if it were
running locally on your machine. This is particularly useful when you want to
run commands inside the container and see their output, or when you need to
provide input to the container's process.
