---
title: MNLS_WideCharToMultiByte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f64cde12-7ed1-444f-8ca4-51cb3ea514cf
description: 'Последнее изменение: 21 февраля 2012 г.'
ms.openlocfilehash: ad41f9b6060e5cfbabecfd9bb29a47815929d6b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338733"
---
# <a name="mnls_widechartomultibyte"></a>MNLS_WideCharToMultiByte

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Эта функция похожа на **WideCharToMultiByte,** которая сопоповедет строку UTF-16 (широкий символ) с новой строкой символов. Новая строка символов не обязательно из многобайтного набора символов.
  
```cpp
int MNLS_WideCharToMultiByte(
  UINT uCodePage,
  DWORD dwFlags,
  LPCWSTR lpWideCharStr,
  int cchWideChar,
  LPSTR lpMultiByteStr,
  int cchMultiByte,
  LPCSTR lpDefaultChar,
  BOOL FAR *lpfUsedDefaultChar);
```

## <a name="parameters"></a>Parameters

 _uCodePage_
  
> [in] Страница кода, используемая для выполнения преобразования.
    
 _dwFlags_
  
> [in] Флаги, указывающие тип преобразования.
    
 _lpWideCharStr_
  
> [in] Указатель на строку Unicode для преобразования.
    
 _cchWideChar_
  
> [in] Флаги, указывающие тип преобразования.
    
 _lpMultiByteStr_
  
> [out] Optional. Указатель на буфер, который получает преобразованную строку.
    
 _cchMultiByte_
  
> [in] Размер в bytes буфера, указанный  _lpMultiByteStr_.
    
 _lpDefaultChar_
  
> [in] Optional. Указатель на символ, который следует использовать, если символ не может быть представлен на указанной странице кода.
    
 _lpfUsedDefaultChar_
  
> [out] Optional. Указатель на флаг, который указывает, использовал ли функция символ по умолчанию в преобразовании.
    
## <a name="return-value"></a>Возвращаемое значение

Возвращает количество bytes, написанных в буфер, на который указывает  _lpMultiByteStr_ в случае успешного списания. 
  
## <a name="remarks"></a>Примечания

Эта функция завершает функцию **WideCharToMultiByte.** Дополнительные сведения см. [в ссылке WideCharToMultiByte.](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx)
  
## <a name="see-also"></a>См. также



[WideCharToMultiByte](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx)

