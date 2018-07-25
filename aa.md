var query = wx.createSelectorQuery();
         query.select('#tabCon').boundingClientRect(function (res) {
              that.setData({
                tabScrollTop: res.top
              })
            }).exec()
