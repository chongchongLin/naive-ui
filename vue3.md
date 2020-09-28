last cherry-picked commit: 4c6b3822293252d461b0a0f3b18b7d2b40bdcf8b

zindexable 最好写成 directive
placeable 进行了大调整


在很特殊的情况下，popover 的在 teleport 打开的时候 beforeUnmount 会被调用两次，具体没有研究出为什么。

- [ ] form
- [x] affix
  - deprecate
    - `target` => `listen-to`
- [x] alert
- [x] anchor
- [ ] auto-complete
- [x] avatar
- [x] back-top
  - new
    - `show` controlled show
    - `on-update:show`
    - `to` teleport target
  - deprecate
    - `on-show` => `on-update:show`
    - `on-hide` => `on-update:show`
    - `target` => `listen-to`
- [x] badge
- [x] breadcrumb
- [x] button
- [x] button-group
- [x] card
- [ ] cascader
- [ ] checkbox
- [x] code
- [x] collapse
  - deprecate
    - `on-expanded-names-change` => `on-update:expanded-names`
  - removed
    - `v-model` => `v-model:expanded-names`
- [x] config-consumer
- [x] config-provider
  - break
    - `$NOs.theme` => `useOsTheme`
  - deprecate
    - `as` => `tag`
  - new
    - provide `useOsTheme` hook
- [x] confirm => `dialog`
  - break
    - rename `confirm` to `dialog`
  - remove
    - `$NConfirm`, `$NModal` => `inject.dialog`
- [ ] data-table
- [ ] date-picker
- [x] descriptions
- [x] divider
- [x] drawer
  - break
    - `v-model`
  - deprecate
    - `on-show` => `on-update:show`
    - `on-hide` => `on-update:show`
    - `target` => `to`
    - `drawer-class` => `body-class`
    - `drawer-style` => `body-style`
  - new
    - `display-directive` prop
- [ ] dropdown
- [ ] dynamic-input
- [ ] dynamic-tags
- [x] element
- [x] empty
- [x] gradient-text
- [x] grid
- [x] icon
- [x] input
  - break
    - `v-model`
  - new
    - `on-update:value`
- [ ] input-group
- [ ] input-group-label
- [ ] input-number
- [x] layout
  - layout-sider
    - deprecate
      - `on-expand` => `on-update:collapsed`
      - `on-collapse` => `on-update:collapsed`
- [x] list
- [x] loading-bar
  - remove
    - `$NLoadingBar`
  - new
    - `n-loading-bar-provider`
- [x] log
- [x] menu
  - new
    - `popover-body-style`
  - deprecate
    - `on-expanded-names-change` => `on-update:expanded-keys`
    - `on-select` => `on-update:model-value`
    - `expanded-names` => `expanded-keys`
    - `default-expanded-names` => `default-expanded-keys`
    - `item.name` => `item.key`
    - `item.titleExtra` => `item.extra`
  - remove
    - `overlay-width`
    - `overlay-min-width`
- [x] message
  - rewrite message using `n-message-provider`
  - deprecate
    - `onHide` => `onLeave`
    - `onAfterHide` => `onAfterLeave`
  - remove
    - `message.hide` => `message.destroy`
- [x] modal
  - rewrite with teleport
  - new
    - `display-directive`
  - deprecate
    - `v-model`
    - `on-show` => `on-update:show`
    - `on-hide` => `on-update:show`
    - `overlay-style` => `body-style`
  - remove
    - default hide behavior for preset
- [x] notification
  - deprecate
    - `open` => `create`
    - `onHide` => `onLeave`
    - `onAfterShow` => `onAfterEnter`
    - `onAfterHide` => `onAfterHide`
- [x] pagination
  - deprecate
    - `on-change` => `on-update:page`
    - `on-page-size-change` => `on-update:page-size`
- [x] popconfirm
- [x] popover
  - new
    - `default-show`
  - deprecate
    - `v-slot:activator` => `v-slot:trigger`
    - `overlay-xxx` => `body-xxx`
  - remove
    - `controller`
    - `max-width`
    - `width`
    - `min-width`
    - `manual` trigger is removed, use `null` instead
  - other
    - set default trigger to `null`
- [ ] popselect
- [x] progress
- [ ] radio
- [x] result
- [ ] scrollbar
- [ ] select
- [ ] slider
- [x] spin
- [x] statistic
- [x] steps
- [x] switch
  - remove
    - `value` => `model-value`
    - `change` => `on-update:model-value`
- [ ] table
- [x] tabs
  - deprecate
    - `active-name` => `value`
    - `on-active-name-change` => `on-update:value`
- [x] tag
  - deprecate
    - `on-checked-change` => `on-update:checked`
- [x] thing
- [x] time
- [ ] time-picker
- [x] timeline
- [x] tooltip
  - ref
- [ ] transfer
- [ ] tree
- [x] typography
- [ ] upload