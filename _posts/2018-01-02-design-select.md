---
layout: post
title:  图案选择
date:   2018-01-02 14:09:47 +0800
categories: specification img
pageName: sample
sorts: [
  { title: VR实景, folder: vr-panorama, pictures: [ ['003', '004'], ['005', '006'], ['007', '008'], ['009', '010'] ]},
  { title: 手工, folder: manual, pictures: [ ['011', '013'], ['014', '015'], ['016', '017'], ['018', '019'], ['020', '021'], ['022', '023'], ['024', '025'], ['026', '027'], ['028', '029'], ['030', '031'], ['032', '033'], ['034', '035'], ['036'] ]},
  { title: 电视墙, folder: tv-wall, pictures: [ ['037', '039'], ['040', '041'], ['042', '043'], ['044', '045'], ['046', '047'], ['048', '049'], ['050', '051'], ['052', '053'], ['054', '055'], ['056', '057'], ['058', '059'], ['060', '061'], ['062', '063'], ['064', '065'], ['066', '068'] ]},
  { title: 沙发墙, folder: sofa-wall, pictures: [ ['069', '071'], ['072', '073'], ['074', '075'], ['076', '077'], ['078', '079'], ['080', '081'], ['082', '083'], ['084', '085'], ['086', '087'], ['088', '089'], ['090', '100'], ['101', '102'] ]},
  { title: 卧室, folder: bedroom, pictures: [ ['103', '105'], ['106', '107'], ['108', '109'], ['110', '111'], ['113', '114'], ['115', '116'], ['117', '118'], ['119', '120'], ['121', '122'], ['123', 124], ['125', '126'] ]},
  { title: 餐厅, folder: dining-room, pictures: [ ['127', '129'], ['130', '131'], ['132', '133'], ['134', '135'], ['136', '137'], ['138', '139'], ['140', '141'], ['142'] ]},
  { title: 儿童房, folder: children-room, pictures: [ ['143', '145'], ['146', '147'], ['148', '149'], ['150', '151'], ['152', '153'], ['154', '155'], ['156', '157'], ['158', '159'], ['160', '161'], ['162', '163'], ['164'] ]},
  { title: 玄关, folder: porch, pictures: [ ['165', '167'], ['168', '169'], ['170', '171'], ['172', '173'], ['174', '175'], ['176', '177'], ['178', '179'], ['180', '181'], ['182', '183'] ]},
]
---
#### 林林总总，选择范围还是蛮大的：
{% for sort in page.sorts %}
<div class="alert alert-info" role="alert">{{ sort.title }} ● 系列</div>
  {% for picture in sort.pictures %}
  <div class="row">
    <div class="col-sm-12 col-md-6">
      <div class="thumbnail">
        <img src="/assets/img/design-select/{{ sort.folder }}/{{ picture[0] }}.jpg"/>
        <div class="caption">
          <p class="text-right">
            <a href="/assets/img/design-select/{{ sort.folder }}/original-size/{{ picture[0] }}.jpg" target="_blank" class="btn btn-success" role="button">原图</a>
          </p>
        </div>
      </div>
    </div>
    {% if picture[1] %}
    <div class="col-sm-12 col-md-6">
      <div class="thumbnail">
        <img src="/assets/img/design-select/{{ sort.folder }}/{{ picture[1] }}.jpg"/>
        <div class="caption">
          <p class="text-right">
            <a href="/assets/img/design-select/{{ sort.folder }}/original-size/{{ picture[1] }}.jpg" target="_blank" class="btn btn-success" role="button">原图</a>
          </p>
        </div>
      </div>
    </div>
    {% endif %}
  </div>
  {% endfor %}
{% endfor %}
