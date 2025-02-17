*   Use `Rails::HTML5::SafeListSanitizer` by default in the Rails 7.1 configuration if it is
    supported.

    Action Text's sanitizer can be configured by setting
    `config.action_text.sanitizer_vendor`. Supported values are `Rails::HTML4::Sanitizer` or
    `Rails::HTML5::Sanitizer`.

    The Rails 7.1 configuration will set this to `Rails::HTML5::Sanitizer` when it is supported, and
    fall back to `Rails::HTML4::Sanitizer`. Previous configurations default to
    `Rails::HTML4::Sanitizer`.

    *Mike Dalessio*

*   Attachables now can override default attachment missing template.

    When rendering Action Text attachments where the underlying attachable model has
    been removed, a fallback template is used. You now can override this template on
    a per-model basis. For example, you could render a placeholder image for a file
    attachment or the text "Deleted User" for a User attachment.

    *Matt Swanson*, *Joel Drapper*

*   Update bundled Trix version from `1.3.1` to `2.0.4`.

    *Sarah Ridge*, *Sean Doyle*

*   Apply `field_error_proc` to `rich_text_area` form fields.

    *Kaíque Kandy Koga*

*   Action Text attachment URLs rendered in a background job (a la Turbo
    Streams) now use `Rails.application.default_url_options` and
    `Rails.application.config.force_ssl` instead of `http://example.org`.

    *Jonathan Hefner*

*   Support `strict_loading:` option for `has_rich_text` declaration

    *Sean Doyle*

*   Update ContentAttachment so that it can encapsulate arbitrary HTML content in a document.

    *Jamis Buck*

*   Fix an issue that caused the content layout to render multiple times when a
    rich_text field was updated.

    *Jacob Herrington*

Please check [7-0-stable](https://github.com/rails/rails/blob/7-0-stable/actiontext/CHANGELOG.md) for previous changes.
