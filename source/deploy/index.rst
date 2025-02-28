.. _cachix-deploy:
    
Cachix Deploy 
=============

.. note:: 
   
   Cachix Deploy is in public beta. This means you won't be charged, as we
   are gathering feedback.
        

`Cachix Deploy <https://app.cachix.org/deploy/>`_ provides continuous deployments to a Nix profile 
(like `NixOS <https://nixos.org>`_, `nix-darwin <https://github.com/LnL7/nix-darwin>`_ or `Home Manager <https://github.com/nix-community/home-manager>`_) using a pull model.

It consists of running a simple daemon process ``cachix deploy agent myagent`` that connects to our backend using websockets and 
waits for a new deployment. There's no Nix evaluation or building done on the agent. The
agent pulls all binaries from your binary cache and activates the new deployment. 

To start new deployments you run ``cachix deploy activate <deploy.json>`` with a specification
of what each agent should deploy.

See `an example of how we deploy our self-managed CI workers <https://github.com/cachix/cachix-ci-agents>`_.

.. toctree::
   :maxdepth: 2
   :glob:

   running-an-agent/index.rst
   deploying-to-agents/index.rst
   reference.rst
