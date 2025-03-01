An open-source color system for building accessible, nice-looking color palettes.

```css
:root {

  --rose-1: #fff7f9;
  --rose-2: #ffdce5;
  --rose-3: #ff3b8d;
  --rose-4: #db0072;
  --rose-5: #800040;
  --rose-6: #4c0023;

  --gray-1: #f6f6f6;
  --gray-2: #e2e2e2;
  --gray-3: #8b8b8b;
  --gray-4: #6f6f6f;
  --gray-5: #3e3e3e;
  --gray-6: #222222;

  --raspberry-1: #fff8f8;
  --raspberry-2: #ffdddf;
  --raspberry-3: #ff426c;
  --raspberry-4: #de0051;
  --raspberry-5: #82002c;
  --raspberry-6: #510018;

  --red-1: #fff8f6;
  --red-2: #ffddd8;
  --red-3: #ff4647;
  --red-4: #e0002b;
  --red-5: #830014;
  --red-6: #530003;

  --orange-1: #fff8f5;
  --orange-2: #ffded1;
  --orange-3: #fd4d00;
  --orange-4: #cd3c00;
  --orange-5: #752100;
  --orange-6: #401600;

  --cinnamon-1: #fff8f3;
  --cinnamon-2: #ffdfc6;
  --cinnamon-3: #d57300;
  --cinnamon-4: #ac5c00;
  --cinnamon-5: #633300;
  --cinnamon-6: #371d00;

  --amber-1: #fff8ef;
  --amber-2: #ffe0b2;
  --amber-3: #b98300;
  --amber-4: #926700;
  --amber-5: #523800;
  --amber-6: #302100;

  --yellow-1: #fff9e5;
  --yellow-2: #ffe53e;
  --yellow-3: #9c8b00;
  --yellow-4: #7d6f00;
  --yellow-5: #463d00;
  --yellow-6: #292300;

  --lime-1: #f7ffac;
  --lime-2: #d5f200;
  --lime-3: #819300;
  --lime-4: #677600;
  --lime-5: #394100;
  --lime-6: #222600;

  --chartreuse-1: #e5ffc3;
  --chartreuse-2: #98fb00;
  --chartreuse-3: #5c9b00;
  --chartreuse-4: #497c00;
  --chartreuse-5: #264500;
  --chartreuse-6: #182600;

  --green-1: #e0ffd9;
  --green-2: #72ff6c;
  --green-3: #00a21f;
  --green-4: #008217;
  --green-5: #004908;
  --green-6: #062800;

  --emerald-1: #dcffe6;
  --emerald-2: #5dffa2;
  --emerald-3: #00a05a;
  --emerald-4: #008147;
  --emerald-5: #004825;
  --emerald-6: #002812;

  --aquamarine-1: #daffef;
  --aquamarine-2: #42ffc6;
  --aquamarine-3: #009f78;
  --aquamarine-4: #007f5f;
  --aquamarine-5: #004734;
  --aquamarine-6: #00281b;

  --teal-1: #d7fff7;
  --teal-2: #00ffe4;
  --teal-3: #009e8c;
  --teal-4: #007c6e;
  --teal-5: #00443c;
  --teal-6: #002722;

  --cyan-1: #c4fffe;
  --cyan-2: #00fafb;
  --cyan-3: #00999a;
  --cyan-4: #007a7b;
  --cyan-5: #004344;
  --cyan-6: #002525;

  --powder-1: #dafaff;
  --powder-2: #8df0ff;
  --powder-3: #0098a9;
  --powder-4: #007987;
  --powder-5: #004048;
  --powder-6: #002227;

  --sky-1: #e3f7ff;
  --sky-2: #aee9ff;
  --sky-3: #0094b4;
  --sky-4: #007590;
  --sky-5: #00404f;
  --sky-6: #001f28;

  --cerulean-1: #e8f6ff;
  --cerulean-2: #b9e3ff;
  --cerulean-3: #0092c5;
  --cerulean-4: #00749d;
  --cerulean-5: #003c54;
  --cerulean-6: #001d2a;

  --azure-1: #e8f2ff;
  --azure-2: #c6e0ff;
  --azure-3: #008fdb;
  --azure-4: #0071af;
  --azure-5: #003b5e;
  --azure-6: #001c30;

  --blue-1: #f0f4ff;
  --blue-2: #d4e0ff;
  --blue-3: #0089fc;
  --blue-4: #006dca;
  --blue-5: #00386d;
  --blue-6: #001a39;

  --indigo-1: #f3f3ff;
  --indigo-2: #deddff;
  --indigo-3: #657eff;
  --indigo-4: #0061fc;
  --indigo-5: #00328a;
  --indigo-6: #001649;

  --violet-1: #f7f1ff;
  --violet-2: #e8daff;
  --violet-3: #9b70ff;
  --violet-4: #794aff;
  --violet-5: #2d0fbf;
  --violet-6: #0b0074;

  --purple-1: #fdf4ff;
  --purple-2: #f7d9ff;
  --purple-3: #d150ff;
  --purple-4: #b01fe3;
  --purple-5: #660087;
  --purple-6: #3a004f;

  --magenta-1: #fff3fc;
  --magenta-2: #ffd7f6;
  --magenta-3: #f911e0;
  --magenta-4: #ca00b6;
  --magenta-5: #740068;
  --magenta-6: #44003c;

  --pink-1: #fff7fb;
  --pink-2: #ffdcec;
  --pink-3: #ff2fb2;
  --pink-4: #d2008f;
  --pink-5: #790051;
  --pink-6: #4b0030;

}
```

```css
.rose-1 {
  background: var(--rose-1);
}
.rose-2 {
  background: var(--rose-2);
}
.rose-3 {
  background: var(--rose-3);
}
.rose-4 {
  background: var(--rose-4);
}
.rose-5 {
  background: var(--rose-5);
}
.rose-6 {
  background: var(--rose-6);
}
.gray-1 {
  background: var(--gray-1);
}
.gray-2 {
  background: var(--gray-2);
}
.gray-3 {
  background: var(--gray-3);
}
.gray-4 {
  background: var(--gray-4);
}
.gray-5 {
  background: var(--gray-5);
}
.gray-6 {
  background: var(--gray-6);
}
.raspberry-1 {
  background: var(--raspberry-1);
}
.raspberry-2 {
  background: var(--raspberry-2);
}
.raspberry-3 {
  background: var(--raspberry-3);
}
.raspberry-4 {
  background: var(--raspberry-4);
}
.raspberry-5 {
  background: var(--raspberry-5);
}
.raspberry-6 {
  background: var(--raspberry-6);
}
.red-1 {
  background: var(--red-1);
}
.red-2 {
  background: var(--red-2);
}
.red-3 {
  background: var(--red-3);
}
.red-4 {
  background: var(--red-4);
}
.red-5 {
  background: var(--red-5);
}
.red-6 {
  background: var(--red-6);
}
.orange-1 {
  background: var(--orange-1);
}
.orange-2 {
  background: var(--orange-2);
}
.orange-3 {
  background: var(--orange-3);
}
.orange-4 {
  background: var(--orange-4);
}
.orange-5 {
  background: var(--orange-5);
}
.orange-6 {
  background: var(--orange-6);
}
.cinnamon-1 {
  background: var(--cinnamon-1);
}
.cinnamon-2 {
  background: var(--cinnamon-2);
}
.cinnamon-3 {
  background: var(--cinnamon-3);
}
.cinnamon-4 {
  background: var(--cinnamon-4);
}
.cinnamon-5 {
  background: var(--cinnamon-5);
}
.cinnamon-6 {
  background: var(--cinnamon-6);
}
.amber-1 {
  background: var(--amber-1);
}
.amber-2 {
  background: var(--amber-2);
}
.amber-3 {
  background: var(--amber-3);
}
.amber-4 {
  background: var(--amber-4);
}
.amber-5 {
  background: var(--amber-5);
}
.amber-6 {
  background: var(--amber-6);
}
.yellow-1 {
  background: var(--yellow-1);
}
.yellow-2 {
  background: var(--yellow-2);
}
.yellow-3 {
  background: var(--yellow-3);
}
.yellow-4 {
  background: var(--yellow-4);
}
.yellow-5 {
  background: var(--yellow-5);
}
.yellow-6 {
  background: var(--yellow-6);
}
.lime-1 {
  background: var(--lime-1);
}
.lime-2 {
  background: var(--lime-2);
}
.lime-3 {
  background: var(--lime-3);
}
.lime-4 {
  background: var(--lime-4);
}
.lime-5 {
  background: var(--lime-5);
}
.lime-6 {
  background: var(--lime-6);
}
.green-1 {
  background: var(--green-1);
}
.green-2 {
  background: var(--green-2);
}
.green-3 {
  background: var(--green-3);
}
.green-4 {
  background: var(--green-4);
}
.green-5 {
  background: var(--green-5);
}
.green-6 {
  background: var(--green-6);
}
.emerald-1 {
  background: var(--emerald-1);
}
.emerald-2 {
  background: var(--emerald-2);
}
.emerald-3 {
  background: var(--emerald-3);
}
.emerald-4 {
  background: var(--emerald-4);
}
.emerald-5 {
  background: var(--emerald-5);
}
.emerald-6 {
  background: var(--emerald-6);
}
.aquamarine-1 {
  background: var(--aquamarine-1);
}
.aquamarine-2 {
  background: var(--aquamarine-2);
}
.aquamarine-3 {
  background: var(--aquamarine-3);
}
.aquamarine-4 {
  background: var(--aquamarine-4);
}
.aquamarine-5 {
  background: var(--aquamarine-5);
}
.aquamarine-6 {
  background: var(--aquamarine-6);
}
.powder-1 {
  background-color: var(--powder-1);
}
.powder-2 {
  background-color: var(--powder-2);
}
.powder-3 {
  background-color: var(--powder-3);
}
.powder-4 {
  background-color: var(--powder-4);
}
.powder-5 {
  background-color: var(--powder-5);
}
.powder-6 {
  background-color: var(--powder-6);
}
.cyan-1 {
  background-color: var(--cyan-1);
}
.cyan-2 {
  background-color: var(--cyan-2);
}
.cyan-3 {
  background-color: var(--cyan-3);
}
.cyan-4 {
  background-color: var(--cyan-4);
}
.cyan-5 {
  background-color: var(--cyan-5);
}
.cyan-6 {
  background-color: var(--cyan-6);
}
.teal-1 {
  background-color: var(--teal-1);
}
.teal-2 {
  background-color: var(--teal-2);
}
.teal-3 {
  background-color: var(--teal-3);
}
.teal-4 {
  background-color: var(--teal-4);
}
.teal-5 {
  background-color: var(--teal-5);
}
.teal-6 {
  background-color: var(--teal-6);
}
.sky-1 {
  background-color: var(--sky-1);
}
.sky-2 {
  background-color: var(--sky-2);
}
.sky-3 {
  background-color: var(--sky-3);
}
.sky-4 {
  background-color: var(--sky-4);
}
.sky-5 {
  background-color: var(--sky-5);
}
.sky-6 {
  background-color: var(--sky-6);
}
.cerulean-1 {
  background-color: var(--cerulean-1);
}
.cerulean-2 {
  background-color: var(--cerulean-2);
}
.cerulean-3 {
  background-color: var(--cerulean-3);
}
.cerulean-4 {
  background-color: var(--cerulean-4);
}
.cerulean-5 {
  background-color: var(--cerulean-5);
}
.cerulean-6 {
  background-color: var(--cerulean-6);
}
.azure-1 {
  background-color: var(--azure-1);
}
.azure-2 {
  background-color: var(--azure-2);
}
.azure-3 {
  background-color: var(--azure-3);
}
.azure-4 {
  background-color: var(--azure-4);
}
.azure-5 {
  background-color: var(--azure-5);
}
.azure-6 {
  background-color: var(--azure-6);
}
.blue-1 {
  background-color: var(--blue-1);
}
.blue-2 {
  background-color: var(--blue-2);
}
.blue-3 {
  background-color: var(--blue-3);
}
.blue-4 {
  background-color: var(--blue-4);
}
.blue-5 {
  background-color: var(--blue-5);
}
.blue-6 {
  background-color: var(--blue-6);
}
.indigo-1 {
  background-color: var(--indigo-1);
}
.indigo-2 {
  background-color: var(--indigo-2);
}
.indigo-3 {
  background-color: var(--indigo-3);
}
.indigo-4 {
  background-color: var(--indigo-4);
}
.indigo-5 {
  background-color: var(--indigo-5);
}
.indigo-6 {
  background-color: var(--indigo-6);
}
.violet-1 {
  background-color: var(--violet-1);
}
.violet-2 {
  background-color: var(--violet-2);
}
.violet-3 {
  background-color: var(--violet-3);
}
.violet-4 {
  background-color: var(--violet-4);
}
.violet-5 {
  background-color: var(--violet-5);
}
.violet-6 {
  background-color: var(--violet-6);
}
.purple-1 {
  background-color: var(--purple-1);
}
.purple-2 {
  background-color: var(--purple-2);
}
.purple-3 {
  background-color: var(--purple-3);
}
.purple-4 {
  background-color: var(--purple-4);
}
.purple-5 {
  background-color: var(--purple-5);
}
.purple-6 {
  background-color: var(--purple-6);
}
.magenta-1 {
  background-color: var(--magenta-1);
}
.magenta-2 {
  background-color: var(--magenta-2);
}
.magenta-3 {
  background-color: var(--magenta-3);
}
.magenta-4 {
  background-color: var(--magenta-4);
}
.magenta-5 {
  background-color: var(--magenta-5);
}
.magenta-6 {
  background-color: var(--magenta-6);
}
.pink-1 {
  background-color: var(--pink-1);
}
.pink-2 {
  background-color: var(--pink-2);
}
.pink-3 {
  background-color: var(--pink-3);
}
.pink-4 {
  background-color: var(--pink-4);
}
.pink-5 {
  background-color: var(--pink-5);
}
.pink-6 {
  background-color: var(--pink-6);
}

```