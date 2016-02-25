# DASHLiveEdgeCalculator
Calculates the live edge for MPEG-DASH segment template based streams. Can be used to analyze segment template based MPEG-DASH MPDs.

**Usage:** CalcLiveEdge availabilityStartTime duration timescale startNumber [start-to-play-time]

# Example
```
<MPD xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:mpeg:dash:schema:mpd:2011" xsi:schemaLocation="urn:mpeg:dash:schema:mpd:2011 http://standards.iso.org/ittf/PubliclyAvailableStandards/MPEG-DASH_schema_files/DASH-MPD.xsd" type="dynamic" availabilityStartTime="2015-03-31T07:28:26Z" timeShiftBufferDepth="PT10S" minimumUpdatePeriod="PT595H" maxSegmentDuration="PT5S" minBufferTime="PT1S" profiles="urn:mpeg:dash:profile:isoff-live:2011">
  <Period id="1" start="PT0S">
    <AdaptationSet group="2" mimeType="video/mp4" segmentAlignment="true">
      <Representation id="250kbps_240p" frameRate="24" bandwidth="250000" codecs="avc1.42c00d" width="420" height="236">
        <SegmentTemplate duration="2000" timescale="1000" media="../dash/250k/bitcodin-$Number$.m4v" initialization="../dash/250k/bitcodin-init.m4v" startNumber="244992"/>
      </Representation>
    </AdaptationSet>
  </Period>
</MPD>
```

**CalcLiveEdge with the MPD above:** java -jar CalcLiveEdge.jar 2015-03-31T07:28:26Z 2000 1000 244992 [20150412T192050]

# MPEG-DASH Content Generation
MPEG-DASH content could be generated with the cloud based transcoding service [bitcodin](http://www.bitcodin.com). Visit [www.bitcodin.com](http://www.bitcodin.com) and experience the fastest way of MPEG-DASH and Apple HLS video transcoding with $ 25 transcoding credit's for free.

[![bitcodin](http://www.bitmovin.net/wp-content/uploads/2015/03/General-Try-Now-1024x538.jpg)](http://www.bitcodin.com)

# MPEG-DASH Players
If your are searching for an MPEG-DASH player visit [dash-player.com](http://www.dash-player.com/).

[![bitdash](http://www.dash-player.com/wp-content/uploads/2015/03/Player.gif)](http://www.dash-player.com/)


