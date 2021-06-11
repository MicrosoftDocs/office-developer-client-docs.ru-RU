---
title: IPSTOVERRIDEREQRegisterTrustedPSTOverrideHandler
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDEREQ.RegisterTrustedPSTOverrideHandler
api_type:
- COM
ms.assetid: 4a73c77c-7e32-4302-bffe-a1ea13574731
description: 'Последнее изменение: 24 февраля 2013 г.'
ms.openlocfilehash: acc0986dd80b549b0cb2b941a6937d47a4a959fe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279537"
---
# <a name="ipstoverridereqregistertrustedpstoverridehandler"></a>IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler

 
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Инициирует процедуру разблокировки для файла личных папок (PST).
  
```cpp
HRESULT RegisterTrustedPSTOverrideHandler (
  LPCWSTR pwzDllPath, 
  LPVOID pvClientData
); 

```

## <a name="parameters"></a>Parameters

 _pwzDllPath_
  
> [in] Указатель на путь сторонних библиотек динамических ссылок (DLL).
    
 _pvClientData_
  
> [in] Указатель на данные клиента, который будет передаваться поставщиком PST в последующие вызовы в функцию HrTrustedPSTOverrideHandlerCallback DLL. Эти клиентские данные могут использоваться DLL для проверки, следует ли разблокировать PST.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Вызов функции был успешным.
    
## <a name="remarks"></a>Примечания

DLL, указанный параметром wzDllPath, должен быть подписан с помощью цифрового сертификата. DLL также должен экспортировать функцию со следующей подписью.
  
```
extern "C" HRESULT __cdecl HrTrustedPSTOverrideHandlerCallback(IMsgStore *pmstore, IUnknown *pOverride, LPVOID pvClientData)
```

Эта функция будет вызвана с указателем на объект IMsgStore для PST, указателем на объект IUnknown, который реализует интерфейс IPSTOVERRIDE1, и указателем на данные, первоначально предоставленные через pvClientData.
  
Дополнительные сведения см. в рубрике Как реализовать обработник переопределения PST для обхода политики [PSTDisableGrow в Outlook 2007 г.](https://support.microsoft.com/kb/956070)
  
## <a name="see-also"></a>См. также



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)
  
[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

