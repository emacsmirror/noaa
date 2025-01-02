# noaa.el

*View a summary of an NOAA weather forecast*

The [NOAA](http://www.noaa.gov) exposes a number of services which
provide weather-related data. **noaa.el** provides an interface for
viewing USA forecast data at api.weather.gov.

---

## Use

1. Use <kbd>M-x</kbd> `noaa` to invoke `noaa`.

2. When done, use <kbd>q</kbd> to invoke `noaa-quit`.

### Configure noaa.el

If `calendar-latitude` and `calendar-latitude` are already defined, those values will be used
when noaa.el initially runs.

If  `calendar-latitude` and `calendar-latitude` are  not already defined, `noaa-latitude` and `noaa-longitude` may be set to the desired values. For example, one might set them via `ielm` (<kbd>M-x</kbd> `ielm`):

    ;; set latitude and longitude for noaa.el
	(setq noaa-latitude 45)
	(setq noaa-longitude 120)

NOAA accepts coordinates as floating point numbers with up to four
digits of precision (eg. 45.1234).


### Additional notes on use

- The header line lists useful keybindings

  - <kbd>n</kbd> to cycle through forecast view styles

  - <kbd>h</kbd> to view an hourly forecast

  - <kbd>d</kbd> to view a daily forecast (the default)

  - <kbd>c</kbd> to view a forecast for a different USA location.

    - If osm.el bookmarks are available, you can select an osm.el bookmark or, if you just press
      <kbd>enter</kbd>, you'll be prompted for latitude and longitude
      coordinates.

  - <kbd>q</kbd> to quit


## osm.el bookmarks

The completion support provided by [vertico](https://github.com/minad/vertico) makes selection of osm.el bookmarks pretty straightforward.


## Customization

The default forecast presentation styles don't present *all* of the
possible data available from NOAA. You can customize the styles by modifying variables `noaa-daily-styles` and
`noaa-hourly-styles` with reference to the NOAA api. Two useful
reference URLs are indicated in the source code.


### Getting started without the Emacs package manager

As noaa.el depends on several packages, it is most straightforward to install it, and the associated dependencies, using the Emacs package manager.

The packages noaa.el leans on are listed in the `(require …)` sexps at the top of the file.

1. Download `noaa.el`.
2. Load `noaa.el`. For example, you might add the following line to `~/.emacs`:

    `(load "/path/to/noaa.el")`


## License

This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.

If you did not receive a copy of the GNU General Public License along with this program, see http://www.gnu.org/licenses/.
