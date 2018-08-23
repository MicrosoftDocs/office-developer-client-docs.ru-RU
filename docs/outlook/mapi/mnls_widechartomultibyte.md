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
ms.openlocfilehash: 6957888f6727175d73d277cf4f5b84dc234d22ea
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570039"
---
# <a name="mnlswidechartomultibyte"></a>MNLS_WideCharToMultiByte

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Эта функция аналогична **WideCharToMultiByte**, которая соответствует строка UTF-16 (двухбайтовых знаков) новую строку знаков. Создать строку знаков не обязательно из многобайтовой задан.
  
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

 _uCodePage_
  
> [in] Кодовая страница следует использовать при выполнении преобразования.
    
 _dwFlags_
  
> [in] Флаги, указывающее тип преобразования.
    
 _lpWideCharStr_
  
> [in] Указатель на строку Юникод для преобразования.
    
 _cchWideChar_
  
> [in] Флаги, указывающее тип преобразования.
    
 _lpMultiByteStr_
  
> [out] Optional. Указатель на буфер, получающий Преобразованная строка.
    
 _cchMultiByte_
  
> [in] Размер, в байтах, указанный в параметре _lpMultiByteStr_буфера.
    
 _lpDefaultChar_
  
> [in] Optional. Указатель на символ для использования, если указанная кодовая страница не может быть представлена знак.
    
 _lpfUsedDefaultChar_
  
> [out] Optional. Указатель на флаг, указывающий, если функция использовал знаков по умолчанию для преобразования.
    
## <a name="return-value"></a>������������ ��������

Возвращает число байт, записанных в буфере, _lpMultiByteStr_ в случае успешного выполнения. 
  
## <a name="remarks"></a>Замечания

Эта функция является функция **WideCharToMultiByte** . Для получения дополнительных сведений см [WideCharToMultiByte](http://msdn.microsoft.com/en-us/library/dd374130%28VS.85%29.aspx).
  
## <a name="see-also"></a>См. также



[WideCharToMultiByte](http://msdn.microsoft.com/en-us/library/dd374130%28VS.85%29.aspx)

