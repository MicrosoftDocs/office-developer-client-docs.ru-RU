---
title: MNLS_MultiByteToWideChar
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 065d78bf-4c9c-48dd-b1f1-b4e59f3f1243
description: 'Last modified: February 21, 2012'
ms.openlocfilehash: 1f137aba40703fe84e5753ee6e370262f780f0a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338243"
---
# <a name="mnls_multibytetowidechar"></a>MNLS_MultiByteToWideChar

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Аналогично **MultiByteToWideChar,** который соповедет строку символов со строкой UTF-16 (широкий символ). Строка символов не обязательно из многобайтового набора символов.
  
```cpp
int MNLS_MultiByteToWideChar(
  UINT uCodePage,
  DWORD dwFlags,
  LPCSTR lpMultiByteStr,
  int cchMultiByte,
  LPWSTR lpWideCharStr,
  int cchWideChar);
```

## <a name="parameters"></a>Параметры

 _uCodePage_
  
> [in] Кодовая страница, используемая для выполнения преобразования.
    
 _dwFlags_
  
> [in] Флаги, указывающие тип преобразования.
    
 _lpMultiByteStr_
  
> [in] Указатель на строку символов для преобразования.
    
 _cchMultiByte_
  
> [in] Размер строки, заданной параметром  _lpMultiByteStr , в 1,6 в 600 000 000 000 000 000 000 000 000 000 000_ 0 
    
 _lpWideCharStr_
  
> [out] Optional. Указатель на буфер, который получает преобразованную строку.
    
 _cchWideChar_
  
> [in] Размер буфера в символах, указанный _lpWideCharStr._
    
## <a name="return-value"></a>Возвращаемое значение

Возвращает количество символов, написанных в буфере,  _обозначенное lpWideCharStr в_ случае успешного успеха. 
  
## <a name="remarks"></a>Примечания

Эта функция обтекает функцию **MultiByteToWideChar.** Дополнительные сведения см. в [подзагоду MultiByteToWideChar.](https://msdn.microsoft.com/library/dd319072%28VS.85%29.aspx)
  

