---
title: MNLS_MultiByteToWideChar
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 065d78bf-4c9c-48dd-b1f1-b4e59f3f1243
description: 'Дата последнего изменения: 21 февраля 2012 г.'
ms.openlocfilehash: 1f137aba40703fe84e5753ee6e370262f780f0a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338243"
---
# <a name="mnls_multibytetowidechar"></a>MNLS_MultiByteToWideChar

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Аналогичен **мултибитетовидечар**, который сопоставляет строку символов со строкой UTF-16 (Wide знака). Строка символов не обязательно должна находиться в многобайтовой кодировке.
  
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

 _укодепаже_
  
> возврата Кодовая страница, используемая для выполнения преобразования.
    
 _dwFlags_
  
> возврата Флаги, указывающие тип преобразования.
    
 _лпмултибитестр_
  
> возврата Указатель на строку символов для преобразования.
    
 _кчмултибите_
  
> возврата Размер (в байтах) строки, указанной параметром _лпмултибитестр_ . 
    
 _лпвидечарстр_
  
> [out] Optional. Указатель на буфер, который получает преобразованную строку.
    
 _кчвидечар_
  
> возврата Размер буфера в символах, указанный в _лпвидечарстр_.
    
## <a name="return-value"></a>Возвращаемое значение

Возвращает число символов, записанных в буфер, указанный в _лпвидечарстр_ в случае успешного выполнения. 
  
## <a name="remarks"></a>Примечания

Эта функция заключает в оболочку функцию **мултибитетовидечар** . Дополнительные сведения см. в разделе [мултибитетовидечар](https://msdn.microsoft.com/library/dd319072%28VS.85%29.aspx).
  

