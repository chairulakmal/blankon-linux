# Wiki Guidelines

This page is for anyone who writes or edits pages in this wiki. It describes how to write and place pages. The most important point: every page is written for its reader, and most readers are BlankOn users who read English as a second language. The page has five parts: where pages go, which language to use, how to write a page, a template for user guides, and how to handle translations.

## Wiki Structure

Document placement must follow the existing structure and conventions. If you are unsure where a document should be placed, please consult with other developers before proceeding.

Directory and file names must use PascalCase (first letter capitalized, no spaces).

## Language

English is preferred for all documentation.

If you are not confident writing in English, you may draft it in Bahasa Indonesia first. Use the English file name and add `.id` before `.md`, for example `Docker.id.md`. Directory and file names must always be written in English.

## Writing a Page

The wiki has two groups of readers. Most are people who use BlankOn. The others are people who contribute to BlankOn. Write user pages so that a new user can follow them without help.

1. **Start with who the page is for.** The first paragraph says who should read the page and what it helps them do.
2. **Use plain English.** Write short sentences with one idea each. Use common words. Avoid idioms and slang.
3. **Explain new terms.** The first time you use a term that a new reader may not know, explain it or link to a page that explains it. BlankOn names such as Sinambung and Arsip are explained in the glossary (`Glossary.md`).
4. **Write exact steps.** Use numbered steps, one action per step. Put each command in a code block. Do not put `$` before a command, so that readers can copy it.
5. **Show how to check the result.** After the steps, tell the reader how to see that it worked.
6. **Link instead of repeating.** If another page already explains something, link to it. Use the full GitHub URL, for example `https://github.com/BlankOn/blankon-linux/blob/main/Goals.md`, because relative links such as `Goals.md` do not work on the BlankOn website.
7. **Keep pages in agreement.** If your page and another page disagree, fix the wrong one in the same pull request.

## User Guide Template

Copy this template for a new page in `UserGuides/`. Remove a section if it does not apply.

````markdown
# Page Title

This page is for <who>. It explains how to <do what>.

## Before You Start

- <What the reader needs first: hardware, packages, settings>

## Steps

1. <One action.>

   ```
   <command>
   ```

2. <Next action.>

## Check the Result

<How the reader can see that it worked.>

## If Something Goes Wrong

<Common problems and their fixes. For other problems, report an issue at https://github.com/BlankOn/blankon-linux/issues.>
````

## Translations

A translation sits next to the original page and has the same name with a language suffix. For example, the Indonesian version of `Docker.md` is `Docker.id.md`.

1. **Translate a page after its content is stable.** A page that still changes often makes the translation fall behind.
2. **Do not translate names, commands or file names.** Write them exactly as in the original.
3. **Keep both versions in agreement.** When you change a page that has a translation, update the translation in the same pull request. If you cannot, open an issue that asks for the translation to be updated.
