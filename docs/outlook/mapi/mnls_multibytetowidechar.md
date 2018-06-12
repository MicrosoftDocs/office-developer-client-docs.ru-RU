---
title: MNLS_MultiByteToWideChar
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 065d78bf-4c9c-48dd-b1f1-b4e59f3f1243
description: 'Последнее изменение: 21 февраля 2012 г.'
ms.openlocfilehash: ab082c8ac70bf851097080fb41033f76bccc3044
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810030"
---
# <a name="mnlsmultibytetowidechar"></a>MNLS_MultiByteToWideChar

  
  
**Применимо к**: Outlook 
  
Аналогично **MultiByteToWideChar**, которая соответствует строка символов строки UTF-16 (двухбайтовых знаков). Строку знаков не обязательно из многобайтовой задан.
  
```cpp
int MNLS_MultiByteToWideChar(
  UINT uCodePage,
  DWORD dwFlags,
  LPCSTR lpMultiByteStr,
  int cchMultiByte,
  LPWSTR lpWideCharStr,
  int cchWideChar);
```

## <a name="parameters"></a>Parameters

 _uCodePage_
  
> [in] Кодовая страница следует использовать при выполнении преобразования.
    
 _dwFlags_
  
> [in] Флаги, указывающее тип преобразования.
    
 _lpMultiByteStr_
  
> [in] Указатель на строку знаков для преобразования.
    
 _cchMultiByte_
  
> [in] Размер, в байтах, указанное с помощью параметра _lpMultiByteStr_ строки. 
    
 _lpWideCharStr_
  
> [out] Optional. Указатель на буфер, получающий Преобразованная строка.
    
 _cchWideChar_
  
> [in] Размер в знаков, указанный в параметре _lpWideCharStr_буфера.
    
## <a name="return-value"></a>������������ ��������

Возвращает число знаков в буфер, указанный в параметре _lpWideCharStr_ в случае успешного выполнения. 
  
## <a name="remarks"></a>Замечания

Эта функция имеет функцию **MultiByteToWideChar** . Для получения дополнительных сведений см [MultiByteToWideChar](http://msdn.microsoft.com/en-us/library/dd319072%28VS.85%29.aspx).
  

