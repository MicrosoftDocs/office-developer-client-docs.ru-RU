---
title: ипстоверридерекрегистертрустедпстоверридехандлер
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
description: 'Дата последнего изменения: 24 февраля 2013 г.'
ms.openlocfilehash: acc0986dd80b549b0cb2b941a6937d47a4a959fe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279537"
---
# <a name="ipstoverridereqregistertrustedpstoverridehandler"></a>IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler

 
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Инициирует процедуру разблокировки для файла личных папок (PST).
  
```cpp
HRESULT RegisterTrustedPSTOverrideHandler (
  LPCWSTR pwzDllPath, 
  LPVOID pvClientData
); 

```

## <a name="parameters"></a>Параметры

 _пвздллпас_
  
> возврата Указатель на путь к сторонней библиотеке динамической компоновки (DLL).
    
 _пвклиентдата_
  
> возврата Указатель на клиентские данные, которые будут переданы поставщиком PST при последующих вызовах функции Хртрустедпстоверридехандлеркаллбакк библиотеки DLL. Эти данные клиента могут использоваться библиотекой DLL для помощи в проверке того, следует ли разблокировать PST-файл.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Вызов функции выполнен успешно.
    
## <a name="remarks"></a>Примечания

Библиотека DLL, заданная параметром Вздллпас, должна быть подписана с помощью цифрового сертификата. Кроме того, Библиотека DLL должна экспортировать функцию со следующей подписью.
  
```
extern "C" HRESULT __cdecl HrTrustedPSTOverrideHandlerCallback(IMsgStore *pmstore, IUnknown *pOverride, LPVOID pvClientData)
```

Эта функция будет вызываться с указателем на объект IMsgStore для PST-файла, указателем на объект IUnknown, который реализует интерфейс IPSTOVERRIDE1, и указателем на данные, изначально предоставленные с помощью Пвклиентдата.
  
Для получения дополнительных сведений Узнайте, [как реализовать обработчик переопределения PST-файлов, чтобы обойти политику пстдисаблегров в Outlook 2007](https://support.microsoft.com/kb/956070).
  
## <a name="see-also"></a>См. также



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)
  
[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

