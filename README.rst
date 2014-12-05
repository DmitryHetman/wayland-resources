========================================
Wayland Resources
========================================

- `Wayland Website <http://wayland.freedesktop.org/>`_
- `Wayland Documentation <http://wayland.freedesktop.org/docs/html/index.html>`_
- `Wayland - ArchWiki <https://wiki.archlinux.org/index.php/wayland>`_

Install
========================================

From ArchWiki
------------------------------

Currently Wayland will only work on systems utilizing KMS.

Wayland is most likely installed on your system already, as it is an indirect dependency of gtk2 and gtk3.

::

    On my Arch Linux computer,
    I already have below shared library in my /usr/lib/ :

        libwayland-client.so
        libwayland-cursor.so
        libwayland-egl.so
        libwayland-server.so


As Wayland is only a library, it is useless on its own. To replace X Server, you need a compositor (like Weston).

Install Weston
------------------------------

.. code-block:: sh

    # Arch Linux

    pacman -S weston

    # It will install
    #
    #   community/libunwind
    #   community/weston

After installed, you can use ``weston`` to run it inside a running X session,
or use ``weston-launch`` to run natively on a tty

.. code-block:: sh

    # run it inside a running X session
    weston

.. image:: images/weston.png
   :alt: picture of weston

.. code-block:: sh

    # run it natively
    weston-launch

