# Pretrained CAMNet Model (SavedModel)

A pretrained CAMNet model is provided as a zipped TensorFlow/Keras SavedModel directory.

## Download Link (Google Drive)

```text
https://drive.google.com/file/d/1ZlRQipx1uNHs0Z8937IXvl4cpcQe6Rad/view?usp=sharing
```

## Extracted Structure

After extracting the zip, you should have a folder similar to:

<pre class="overflow-visible! px-0!" data-start="448" data-end="538"><div class="contain-inline-size rounded-2xl corner-superellipse/1.1 relative bg-token-sidebar-surface-primary"><div class="sticky top-[calc(var(--sticky-padding-top)+9*var(--spacing))]"><div class="absolute end-0 bottom-0 flex h-9 items-center pe-2"><div class="bg-token-bg-elevated-secondary text-token-text-secondary flex items-center gap-4 rounded-sm px-2 font-sans text-xs"></div></div></div><div class="overflow-y-auto p-4" dir="ltr"><code class="whitespace-pre! language-text"><span><span>camnet_savedmodel/
  saved_model.pb
  keras_metadata.pb
  variables/
  assets/
</span></span></code></div></div></pre>

Do not delete or rename files inside the SavedModel directory.

## How to Use (CAMNet Notebook)

1. Open:

* `notebooks/2_camnet_train_or_infer.ipynb`

2. Set:

<pre class="overflow-visible! px-0!" data-start="699" data-end="732"><div class="contain-inline-size rounded-2xl corner-superellipse/1.1 relative bg-token-sidebar-surface-primary"><div class="sticky top-[calc(var(--sticky-padding-top)+9*var(--spacing))]"><div class="absolute end-0 bottom-0 flex h-9 items-center pe-2"><div class="bg-token-bg-elevated-secondary text-token-text-secondary flex items-center gap-4 rounded-sm px-2 font-sans text-xs"></div></div></div><div class="overflow-y-auto p-4" dir="ltr"><code class="whitespace-pre! language-python"><span><span>MODE = </span><span>"pretrained"</span><span>
</span></span></code></div></div></pre>

3. When prompted, provide the path to the extracted SavedModel folder.

The model is loaded using:

* `tf.keras.models.load_model(path, compile=False)`
