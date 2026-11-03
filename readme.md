# Shapes Lab

An educational library written in Fearless.
The library teaches sealed types with shapes made of unit cells on a grid.
The demo is listed in the storefront https://marcoservetto.github.io/fearless_demos/ with the rank `worker100`.

## Use

The URL of the zip is https://marcoautomation2.github.io/shapes_lab/shapes_lab_edu_lib.zip.
The page https://marcoautomation2.github.io/shapes_lab/ has a button that copies the URL.
Import the URL into a Fearless project with the Fearless manager.
The zip also works by hand: copy the zip, zipped or unzipped, into the project.
Write `use shapes_lab.Shapes as Shapes;` in the rank file of the package that needs `Shapes`.
The package that uses the library needs a rank higher than `worker100`.
Every package of rank `app` qualifies.

## The lessons

The package is `shapes_lab`.
Each lesson is one file of the folder `project/_shapes_lab`, and the doc comments of the file are the text of the lesson.
1. `shape.fear`: the sealed type `Shape` and its `.match`.
2. `shapes.fear`: the factories `Shapes.rect`, `Shapes.square` and `Shapes.plus`, which hide the kinds of shapes.
3. `bounds.fear`: methods over lists of shapes.

Every method has examples in its doc comment.
Running the folder `project` checks the examples.
A package inside a zip gets no generated checks, so check the examples with the unzipped folder `project`.

## The example

The folder `example` is a small app that uses the library.
Copy `shapes_lab_edu_lib.zip` into the folder `example`, or copy the folder `project/_shapes_lab` into the folder `example`.
Run the folder `example`.

## Exercises

1. Add a kind `.ell` to `ShapeMatch`, and follow the errors of the compiler to every `.match` that needs a new case.
2. Try to write a type in another package that extends `Shape`, and read the error.

## Deployment

Each push to `main` runs `.github/workflows/pages.yml`.
The workflow zips the folder `project` into `shapes_lab_edu_lib.zip`.
The workflow publishes the zip and `site/index.html` on GitHub Pages.
