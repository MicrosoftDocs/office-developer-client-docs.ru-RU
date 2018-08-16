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
ms.openlocfilehash: 4fc3b7427fc13a024aab38c7b7df1d940a4730ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809563"
---
# <a name="ipstoverridereqregistertrustedpstoverridehandler"></a>IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler

 
  
**Относится к**: Outlook 
  
Инициирует разблокировка процедура файл личных папок (PST).
  
```cpp
HRESULT RegisterTrustedPSTOverrideHandler (
  LPCWSTR pwzDllPath, 
  LPVOID pvClientData
); 

```

## <a name="parameters"></a>Параметры

 _pwzDllPath_
  
> [in] Указатель на путь сторонних производителей библиотеки динамической компоновки (DLL).
    
 _pvClientData_
  
> [in] Указатель на данные клиента, которые будут передаваться поставщиком PST-файлов в последующие вызовы функции HrTrustedPSTOverrideHandlerCallback библиотеки DLL. Эти данные клиента могут быть использованы с библиотеки DLL для помощи при проверке, следует ли разблокированными PST-файлов.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK
  
> Вызов функции прошла успешно.
    
## <a name="remarks"></a>Замечания

DLL, указанного с помощью параметра wzDllPath должны быть подписаны цифровым сертификатом. Библиотеки DLL необходимо экспортировать функции с указанной ниже сигнатурой.
  
```
extern "C" HRESULT __cdecl HrTrustedPSTOverrideHandlerCallback(IMsgStore *pmstore, IUnknown *pOverride, LPVOID pvClientData)
```

Эта функция будет вызываться с указатель на объект IMsgStore для PST-файлов, указатель на объект IUnknown, который реализует интерфейс IPSTOVERRIDE1 и указатель на данные, изначально обеспечиваться pvClientData.
  
Дополнительные сведения см в [реализации обработчика переопределение PST-файлов для обхода политики PSTDisableGrow в Outlook 2007](http://support.microsoft.com/kb/956070).
  
## <a name="see-also"></a>См. также



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)
  
[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)
