---
title: IMAPIViewContextGetPrintSetup
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetPrintSetup
api_type:
- COM
ms.assetid: eaf3bafb-975d-42c8-99ea-7f9ef9c934ba
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 7fdf76bc56feb7e46370e7fcf66c55d229933eca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809257"
---
# <a name="imapiviewcontextgetprintsetup"></a>IMAPIViewContext::GetPrintSetup

  
  
**Относится к**: Outlook 
  
Извлекает сведения о текущем печати.
  
```cpp
HRESULT GetPrintSetup(
ULONG ulFlags,
LPFORMPRINTSETUP FAR * lppFormPrintSetup
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] Битовая маска флаги, определяющее тип возвращенных строк. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> В формате Юникод, возвращенных строк. Если флаг MAPI_UNICODE не установлен, они в формате ANSI.
    
 _lppFormPrintSetup_
  
> [out] Указатель на указатель на структуру, которая содержит сведения о печати.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Печать информации был успешно извлечен.
    
## <a name="remarks"></a>Замечания

Объекты формы вызовите метод **IMAPIViewContext::GetPrintSetup** для получения сведений о настройке принтера прежде чем печати текущего сообщения. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Выделите **hDevMode** и **hDevName** элементы структуры [FORMPRINTSETUP](formprintsetup.md) , с помощью функции Win32 **GlobalAlloc**.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Если предполагается, что **hDevMode** и **hDevName** элементы структуры **FORMPRINTSETUP** указывает параметр _lppFormPrintSetup_ строки Юникод, значение MAPI_UNICODE _ulFlags_ . В противном случае **GetPrintSetup** возвращает эти строки в формате ANSI. 
  
Бесплатная загрузка **hDevMode** и **hDevName** элементы структуры **FORMPRINTSETUP** путем вызова функции Win32 **GlobalFree**. Освободите всю структуру **FORMPRINTSETUP** путем вызова метода [MAPIFreeBuffer](mapifreebuffer.md). 
  
## <a name="see-also"></a>См. также



[FORMPRINTSETUP](formprintsetup.md)
  
[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)

