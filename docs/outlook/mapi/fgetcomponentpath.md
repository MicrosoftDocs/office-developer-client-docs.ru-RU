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
ms.openlocfilehash: e4bce7f122522532023d18b43fe4bfdeda84af9b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808422"
---
# <a name="fgetcomponentpath"></a>FGetComponentPath

  
  
**Относится к**: Outlook 
  
Возвращает путь к частной Mapi32.dll.
  
```cpp
BOOL FGetComponentPath(
  LPCSTR szComponent,
  LPSTR szQualifier,
  LPSTR szDllPath,
  DWORD cchBufferSize,
  BOOL fInstall
);
```

## <a name="parameters"></a>Параметры

 _szComponent_
  
> [in] Раздел реестра MSIComponentID, описанные в [Параметры реестра заглушка Mapi32.dll](http://msdn.microsoft.com/en-us/library/dd162409.aspx).
    
 _szQualifier_
  
> [in] Подраздел MSIApplicationLCID или MSIOfficeLCID, описанных в [выберите определенные версии MAPI для загрузки](how-to-choose-a-specific-version-of-mapi-to-load.md). Вызывающие объекты можно передать **значение null** , если нет квантор. 
    
 _szDllPath_
  
> [in] Путь к частной Mapi32.dll, имеющем полной функциональности MAPI (же экспортирует в виде Mapi32.dll).
    
 _cchBufferSize_
  
> [in] Размер _szDllPath_, в символы.
    
 _fInstall_
  
> [in] Указывает MAPI для установки частный Mapi32.dll компонент, если он отсутствует.
    
## <a name="return-value"></a>������������ ��������

 **значение true**
  
> Найти путь.
    
 **false**
  
> Путь не найден.
    
## <a name="remarks"></a>Замечания

Используйте функцию **FGetComponentPath** , если вам нужно получить путь к частной Mapi32.dll. 
  
## <a name="see-also"></a>См. также



[Выбор определенной версии MAPI для загрузки](how-to-choose-a-specific-version-of-mapi-to-load.md)


[Параметры реестра заглушка Mapi32.dll](http://msdn.microsoft.com/en-us/library/dd162409.aspx)

