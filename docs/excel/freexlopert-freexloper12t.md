---
title: FreeXLOperT/FreeXLOper12T
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FreeXLOper12T
- FreeXLOperT
keywords:
- функция freexlopert [excel 2007], функция FreeXLOper12T [Excel 2007]
localization_priority: Normal
ms.assetid: 8fb3fdfd-8a43-4c50-82ff-e701fed3d83f
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: b7411bc51770dadc7c2d4a5c2c65d2d546f6025f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807262"
---
# <a name="freexlopertfreexloper12t"></a>FreeXLOperT/FreeXLOper12T

 **Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Функция Framework, освобождает память, связанные с **XLOPER**/ **XLOPER12**. Функция предполагается, что объем памяти выделена с вызовы malloc в библиотеке DLL. Если было выделить память с Microsoft Excel или каким-либо другим образом или другим процессом, эта функция не предназначена освободить память. Используйте [xlFree](xlfree.md) , чтобы освободить память, выделенную Excel для **XLOPER**/ **XLOPER12**s. 
  
```cs
void FreeXLOperT(LPXLOPER pxloper);
void FreeXLOper12T(LPXLOPER12 pxloper12);
```

## <a name="parameters"></a>Параметры

 _pxloper_ (**LPXLOPER**)
  
 _pxloper12_ (**LPXLOPER12**)
  
Указатель на **структуру XLOPER**/ **XLOPER12** освобождения. 
  
## <a name="example"></a>Пример

 `\SAMPLES\FRAMEWRK\FRAMEWRK.C`
  
```cs
void FreeXLOper12T(LPXLOPER12 pxloper12)
{
   DWORD xltype;
   int cxloper12;
   LPXLOPER12 pxloper12Free;
   xltype = pxloper12->xltype;
   switch (xltype)
   {
   case xltypeStr:
      if (pxloper12->val.str != NULL)
         free(pxloper12->val.str);
      break;
   case xltypeRef:
      if (pxloper12->val.mref.lpmref != NULL)
         free(pxloper12->val.mref.lpmref);
      break;
   case xltypeMulti:
      cxloper12 = pxloper12->val.array.rows * pxloper12->val.array.columns;
      if (pxloper12->val.array.lparray)
      {
         pxloper12Free = pxloper12->val.array.lparray;
         while (cxloper12 > 0)
         {
            FreeXLOper12T(pxloper12Free);
            pxloper12Free++;
            cxloper12--;
         }
         free(pxloper12->val.array.lparray);
      }
      break;
   case xltypeBigData:
      if (pxloper12->val.bigdata.h.lpbData != NULL)
         free(pxloper12->val.bigdata.h.lpbData);
      break;
   }
}
```

## <a name="see-also"></a>См. также



[Функции в библиотеке платформы](functions-in-the-framework-library.md)

