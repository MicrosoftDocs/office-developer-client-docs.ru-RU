---
title: MNLS_WideCharToMultiByte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f64cde12-7ed1-444f-8ca4-51cb3ea514cf
description: 'Дата последнего изменения: 21 февраля 2012 г.'
ms.openlocfilehash: ad41f9b6060e5cfbabecfd9bb29a47815929d6b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338733"
---
# <a name="mnls_widechartomultibyte"></a>MNLS_WideCharToMultiByte

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Эта функция аналогична **видечартомултибите**, которая СОПОСТАВЛЯЕТ строку UTF-16 (Wide знака) с новой строкой символов. Новая строка символов не обязательно должна быть из многобайтового набора символов.
  
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

## <a name="parameters"></a>Параметры

 _укодепаже_
  
> возврата Кодовая страница, используемая для выполнения преобразования.
    
 _dwFlags_
  
> возврата Флаги, указывающие тип преобразования.
    
 _лпвидечарстр_
  
> возврата Указатель на строку Юникода для преобразования.
    
 _кчвидечар_
  
> возврата Флаги, указывающие тип преобразования.
    
 _лпмултибитестр_
  
> [out] Optional. Указатель на буфер, который получает преобразованную строку.
    
 _кчмултибите_
  
> возврата Размер буфера (в байтах), указанного в _лпмултибитестр_.
    
 _лпдефаултчар_
  
> [in] Optional. Указатель на символ, который будет использоваться, если символ не может быть представлен на указанной кодовой странице.
    
 _лпфуседдефаултчар_
  
> [out] Optional. Указатель на флаг, указывающий, использовался ли для функции символ по умолчанию в преобразовании.
    
## <a name="return-value"></a>Возвращаемое значение

Возвращает число байтов, записанных в буфер, на который указывает _лпмултибитестр_ в случае успешного выполнения. 
  
## <a name="remarks"></a>Примечания

Эта функция заключает в оболочку функцию **видечартомултибите** . Дополнительные сведения см. в разделе [видечартомултибите](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx).
  
## <a name="see-also"></a>См. также



[видечартомултибите](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx)

