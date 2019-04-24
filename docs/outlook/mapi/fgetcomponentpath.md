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
  
Возвращает путь к закрытой MAPI32. dll.
  
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

 _Сзкомпонент_
  
> возврата Ключ Мсикомпонентид reg, описанный в [разделе Параметры реестра MAPI32. dll-заглушек](https://msdn.microsoft.com/library/dd162409.aspx).
    
 _Сзкуалифиер_
  
> возврата Подраздел МсиаппликатионлЦид или МсиоффицелЦид, описанный в статье [Выбор определенной версии MAPI для загрузки](how-to-choose-a-specific-version-of-mapi-to-load.md). Вызывающие абоненты могут передавать **значение NULL** , если нет квалификатора. 
    
 _Сздллпас_
  
> возврата Путь к частному MAPI32. dll, который имеет полную функциональность MAPI (те же экспортируемые компоненты, что и в MAPI32. dll).
    
 _Кчбуфферсизе_
  
> возврата Размер _сздллпас_в символах.
    
 _Финсталл_
  
> возврата Указывает MAPI для установки закрытого компонента MAPI32. dll (если он отсутствует).
    
## <a name="return-value"></a>Возвращаемое значение

 **относится**
  
> Найден путь.
    
 **значения**
  
> Путь не найден.
    
## <a name="remarks"></a>Комментарии

Используйте функцию **фжеткомпонентпас** , если вам нужно получить путь к закрытой MAPI32. dll. 
  
## <a name="see-also"></a>См. также



[Выбор определенной версии MAPI для загрузки](how-to-choose-a-specific-version-of-mapi-to-load.md)


[Параметры реестра для заглушки MAPI32. dll](https://msdn.microsoft.com/library/dd162409.aspx)

