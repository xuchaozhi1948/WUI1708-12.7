# WUI1708-12.7
$zdy:auto;
$ccyc:hidden;
$qzzdy:auto!important;
$nbbk: border-box;
$bfb:100%;
$stat:1;
$pading:15px;
$left:left;
$clear:both;
$display:block;
$over:12;
.container,.container-fluid{
  height: $zdy;
  overflow: $ccyc;
  margin-left: $qzzdy;
  margin-right: $qzzdy;
  box-sizing: $nbbk;
}
.row{
  width: $bfb;
  height: $zdy;
  overflow:$ccyc;
  box-sizing:$nbbk;
  &:before,&:after{content:"";
    display:$display;
    width :0;
    height: 0;
    line-height:0;
    clear:$clear;}
}
[class*="col-"]{
  float: $left;
  padding-left: $pading;
  padding-right: $pading;
  box-sizing: $nbbk;
}
@mixin xun($pmfl,$over){
  @for $stat from 1 through $over{
    .col-#{$pmfl}-#{$stat}{
      width: 1/$over*100%*$stat;

    }
  }
}
@media screen and (max-width:768px){@include xun(xs,$over);}
@media screen and (min-width:768px) and (max-width: 992px){@include xun(sm,$over);}
@media screen and (min-width:992px) and (max-width: 1200px){@include xun(md,$over);}
@media screen and (min-width:1200px){@include xun(lg,$over);}
