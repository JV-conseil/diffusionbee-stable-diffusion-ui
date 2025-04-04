# How to run DiffusionBee from source

Install the following

1. Miniforge [`brew install --cask miniforge`](https://formulae.brew.sh/cask/miniforge)
2. Nodejs v16

Clone the repo:

```sh
git clone https://github.com/divamgupta/diffusionbee-stable-diffusion-ui
```

Create the conda environment and activate it

```sh
cd "${HOME}/GitHub/JV-conseil/diffusionbee-stable-diffusion-ui/backends/stable_diffusion"
conda deactivate
conda create -n diffusion_bee_env python=3.12.9
conda activate diffusion_bee_env
```

Install the python packages

```sh
which pip
pip install -r ./requirements.txt
```

Install the npm packages

```sh
cd "${HOME}/GitHub/JV-conseil/diffusionbee-stable-diffusion-ui/electron_app"
```

npm install

```sh
npm install
```

or yarn install

```sh
yarn set version stable &&
    yarn install
yarn up
yarn npm audit
npx depcheck --detailed
yarn upgrade-interactive
```

Run the app

```sh
npm run electron:serve
```

or

```sh
yarn run electron:serve
```
