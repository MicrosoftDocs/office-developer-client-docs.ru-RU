---
title: FGetComponentPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FGetComponentPath
api_type:
- COM
ms.assetid: 2a303458-3283-409a-bc3b-b891f3fcfc22
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 3456d81935a0a94bc2158eefd321da968dda9983
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335212"
---
# <a name="fgetcomponentpath"></a>FGetComponentPath

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает путь к частному Mapi32.dll.
  
```cpp
BOOL FGetComponentPath(
  LPCSTR szComponent,
  LPSTR szQualifier,
  LPSTR szDllPath,
  DWORD cchBufferSize,
  BOOL fInstall
);
```

## <a name="parameters"></a>Parameters

 _szComponent_
  
> [in] Ключ reg MSIComponentID, описанный вMapi32.dll [реестра Stub Параметры](https://msdn.microsoft.com/library/dd162409.aspx).
    
 _szQualifier_
  
> [in] Подкайка MSIApplicationLCID или MSIOfficeLCID, описанная в "Выбор определенной версии [MAPI для загрузки".](how-to-choose-a-specific-version-of-mapi-to-load.md) Если нет квалификатора, звонители могут передать **null.** 
    
 _szDllPath_
  
> [in] Путь к частному Mapi32.dll, который имеет полный функционал MAPI (тот же экспорт, что и Mapi32.dll).
    
 _cchBufferSize_
  
> [in] Размер  _szDllPath_ в символах.
    
 _fInstall_
  
> [in] Сообщает MAPI установить частный компонент Mapi32.dll, если он отсутствует.
    
## <a name="return-value"></a>Возвращаемое значение

 **true**
  
> Путь найден.
    
 **false**
  
> Путь не найден.
    
## <a name="remarks"></a>Примечания

Используйте **функцию FGetComponentPath** для получения пути к частному Mapi32.dll. 
  
## <a name="see-also"></a>См. также



[Выберите определенную версию MAPI для загрузки](how-to-choose-a-specific-version-of-mapi-to-load.md)


[Mapi32.dll реестра Stub Параметры](https://msdn.microsoft.com/library/dd162409.aspx)

