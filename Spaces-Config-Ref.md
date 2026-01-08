\# Spaces Configuration Reference



Spaces are configured through the `YAML` block at the top of the \*\*README.md\*\* file at the root of the repository. All the accepted parameters are listed below.



\*\*`title`\*\* : \_string\_  

Display title for the Space.  



\*\*`emoji`\*\* : \_string\_  

Space emoji (emoji-only character allowed).  



\*\*`colorFrom`\*\* : \_string\_  

Color for Thumbnail gradient (red, yellow, green, blue, indigo, purple, pink, gray).  



\*\*`colorTo`\*\* : \_string\_  

Color for Thumbnail gradient (red, yellow, green, blue, indigo, purple, pink, gray).  



\*\*`sdk`\*\* : \_string\_  

Can be either `gradio`, `docker`, or `static`.  



\*\*`python\_version`\*\*: \_string\_  

Any valid Python `3.x` or `3.x.x` version.  

Defaults to `3.10`.  



\*\*`sdk\_version`\*\* : \_string\_  

Specify the version of Gradio to use.

All versions of Gradio are supported.  



\*\*`suggested\_hardware`\*\* : \_string\_  

Specify the suggested \[hardware](https://huggingface.co/docs/hub/spaces-gpus) on which this Space must be run.  

Useful for Spaces that are meant to be duplicated by other users.  

Setting this value will not automatically assign an hardware to this Space.  

Value must be a valid hardware flavor. Current valid hardware flavors:

\- CPU: `"cpu-basic"`, `"cpu-upgrade"`

\- GPU: `"t4-small"`, `"t4-medium"`, `"l4x1"`,

&nbsp;	`"l4x4"`, `"a10g-small"`, `"a10g-large"`, `"a10g-largex2"`,

&nbsp;	`"a10g-largex4"`,`"a100-large"`

\- TPU: `"v5e-1x1"`, `"v5e-2x2"`, `"v5e-2x4"`



\*\*`suggested\_storage`\*\* : \_string\_  

Specify the suggested \[permanent storage](https://huggingface.co/docs/hub/spaces-storage) on which this Space must be run.  

Useful for Spaces that are meant to be duplicated by other users.  

Setting this value will not automatically assign a permanent storage to this Space.  

Value must be one of `"small"`, `"medium"` or `"large"`.  



\*\*`app\_file`\*\* : \_string\_  

Path to your main application file (which contains either `gradio` Python code or `static` html code).  

Path is relative to the root of the repository.  



\*\*`app\_build\_command`\*\* : \_string\_  

For static Spaces, command to run first to generate the HTML to render. Example: `npm run build`. 



This is used in conjunction with `app\_file` which points to the built index file: e.g. `app\_file: dist/index.html`. 



Each update, the build command will run in a Job and the build output will be stored in `refs/convert/build`,

which will be served by the Space. See an example at https://huggingface.co/spaces/coyotte508/static-vite



\*\*`app\_port`\*\* : \_int\_  

Port on which your application is running. Used only if `sdk` is `docker`. Default port is `7860`.



\*\*`base\_path`\*\*: \_string\_

For non-static Spaces, initial url to render. Needs to start with `/`. For static Spaces, use `app\_file` instead.



\*\*`fullWidth`\*\*: \_boolean\_  

Whether your Space is rendered inside a full-width (when `true`) or fixed-width column (ie. "container" CSS) inside the iframe.

Defaults to `true`.



\*\*`header`\*\*: \_string\_  

Can be either `mini` or `default`. If `header` is set to `mini` the space will be displayed full-screen with a mini floating header .   



\*\*`short\_description`\*\*: \_string\_

A short description of the Space. This will be displayed in the Space's thumbnail.



\*\*`models`\*\* : \_List\[string]\_  

HF model IDs (like `openai-community/gpt2` or `deepset/roberta-base-squad2`) used in the Space.

Will be parsed automatically from your code if not specified here.  



\*\*`datasets`\*\* : \_List\[string]\_  

HF dataset IDs (like `mozilla-foundation/common\_voice\_13\_0` or `oscar-corpus/OSCAR-2109`) used in the Space.

Will be parsed automatically from your code if not specified here.  



\*\*`tags`\*\* : \_List\[string]\_  

List of terms that describe your Space task or scope.  



\*\*`thumbnail`\*\*: \_string\_  

URL for defining a custom thumbnail for social sharing.



\*\*`pinned`\*\* : \_boolean\_  

Whether the Space stays on top of your profile. Can be useful if you have a lot of Spaces so you and others can quickly see your best Space.  



\*\*`hf\_oauth`\*\* : \_boolean\_  

Whether a connected OAuth app is associated to this Space. See \[Adding a Sign-In with HF button to your Space](https://huggingface.co/docs/hub/spaces-oauth) for more details.



\*\*`hf\_oauth\_scopes`\*\* : \_List\[string]\_

Authorized scopes of the connected OAuth app. `openid` and `profile` are authorized by default and do not need this parameter. See \[Adding a Sign-In with HF button to your space](https://huggingface.co/docs/hub/spaces-oauth) for more details.



\*\*`hf\_oauth\_expiration\_minutes`\*\* : \_int\_

Duration of the OAuth token in minutes. Defaults to 480 minutes (8 hours). Maximum duration is 43200 minutes (30 days). See \[Adding a Sign-In with HF button to your space](https://huggingface.co/docs/hub/spaces-oauth) for more details.



\*\*`hf\_oauth\_authorized\_org`\*\* : \_string\_ or \_List\[string]\_

Restrict OAuth access to members of specific organizations. See \[Adding a Sign-In with HF button to your space](https://huggingface.co/docs/hub/spaces-oauth) for more details.



\*\*`disable\_embedding`\*\* : \_boolean\_  

Whether the Space iframe can be embedded in other websites.

Defaults to false, i.e. Spaces \*can\* be embedded.



\*\*`startup\_duration\_timeout`\*\*: \_string\_  

Set a custom startup duration timeout for your Space. This is the maximum time your Space is allowed to start before it times out and is flagged as unhealthy.

Defaults to 30 minutes, but any valid duration (like `1h`, `30m`) is acceptable.



\*\*`custom\_headers`\*\* : \_Dict\[string, string]\_  

Set custom HTTP headers that will be added to all HTTP responses when serving your Space.  

For now, only the \[cross-origin-embedder-policy](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Cross-Origin-Embedder-Policy) (COEP), \[cross-origin-opener-policy](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Cross-Origin-Opener-Policy) (COOP), and \[cross-origin-resource-policy](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Cross-Origin-Resource-Policy) (CORP) headers are allowed. These headers can be used to set up a cross-origin isolated environment and enable powerful features like `SharedArrayBuffer`, for example:



```yaml

custom\_headers:

&nbsp; cross-origin-embedder-policy: require-corp

&nbsp; cross-origin-opener-policy: same-origin

&nbsp; cross-origin-resource-policy: cross-origin

```



\*Note:\* all headers and values must be lowercase.



\*\*`preload\_from\_hub`\*\*: \_List\[string]\_

Specify a list of Hugging Face Hub models or other large files to be preloaded during the build time of your Space. This optimizes the startup time by having the files ready when your application starts. This is particularly useful for Spaces that rely on large models or datasets that would otherwise need to be downloaded at runtime.



The format for each item is `"repository\_name"` to download all files from a repository, or `"repository\_name file1,file2"` for downloading specific files within that repository. You can also specify a specific commit to download using the format `"repository\_name file1,file2 commit\_sha256"`. 



Example usage:

```yaml

preload\_from\_hub:

&nbsp; - warp-ai/wuerstchen-prior text\_encoder/model.safetensors,prior/diffusion\_pytorch\_model.safetensors

&nbsp; - coqui/XTTS-v1

&nbsp; - openai-community/gpt2 config.json 11c5a3d5811f50298f278a704980280950aedb10

```

In this example, the Space will preload specific .safetensors files from `warp-ai/wuerstchen-prior`, the complete `coqui/XTTS-v1` repository, and a specific revision of the `config.json` file in the `openai-community/gpt2` repository from the Hugging Face Hub during build time.



> \[!WARNING]

> Files are saved in the default `huggingface\_hub` disk cache `~/.cache/huggingface/hub`. If you application expects them elsewhere or you changed your `HF\_HOME` variable, this pre-loading does not follow that at this time.





