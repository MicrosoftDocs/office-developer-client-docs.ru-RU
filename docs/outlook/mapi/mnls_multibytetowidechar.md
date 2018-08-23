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
ms.openlocfilehash: 66e8c3b61caac6fb8d8b57d74ade6fa8aac3a9dd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571709"
---
# <a name="mnlsmultibytetowidechar"></a>MNLS_MultiByteToWideChar

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
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

## <a name="parameters"></a>Параметры

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
  

