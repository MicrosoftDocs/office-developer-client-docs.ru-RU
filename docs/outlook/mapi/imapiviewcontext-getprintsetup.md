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
ms.openlocfilehash: a58e723113f70c10b5c8468f5bdd0d8d9014bd2c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425129"
---
# <a name="imapiviewcontextgetprintsetup"></a>IMAPIViewContext::GetPrintSetup

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Извлекает текущие сведения о печати.
  
```cpp
HRESULT GetPrintSetup(
ULONG ulFlags,
LPFORMPRINTSETUP FAR * lppFormPrintSetup
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет типом возвращаемой строки. Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Возвращенные строки имеют формат Юникод. Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI.
    
 _lppFormPrintSetup_
  
> [out] Указатель на указатель на структуру, которая содержит сведения о печати.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Сведения о печати были успешно извлечены.
    
## <a name="remarks"></a>Примечания

Объекты форм вызовите метод **IMAPIViewContext::GetPrintSetup,** чтобы получить сведения о настройке принтера перед попыткой распечатать текущее сообщение. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

**Выделите члены hDevMode** и **hDevName** структуры [FORMPRINTSETUP](formprintsetup.md) с помощью функции Win32 **GlobalAlloc.**
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Если предполагается, что члены **hDevMode** и **hDevName** структуры **FORMPRINTSETUP,** на которые указывает параметр  _lppFormPrintSetup,_ будут строками Юникода, установите  _для ulFlags_ MAPI_UNICODE. В **противном случае GetPrintSetup** вернет эти строки в формате ANSI. 
  
Освободите **члены hDevMode** и **hDevName** структуры **FORMPRINTSETUP,** вызывая функцию Win32 **GlobalFree.** Освободите всю **структуру FORMPRINTSETUP,** вызывая [MAPIFreeBuffer.](mapifreebuffer.md) 
  
## <a name="see-also"></a>См. также



[FORMPRINTSETUP](formprintsetup.md)
  
[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)

