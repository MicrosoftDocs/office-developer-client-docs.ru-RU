---
title: Функция DOCMD
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60100
localization_priority: Normal
ms.assetid: 6574edeb-eb6f-afd9-89c4-eb5996dffa30
description: Выполняет установленную команду.
ms.openlocfilehash: 9e5c02c9a90f3aab66c5d582c83d7d9d892f964c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413075"
---
# <a name="docmd-function"></a>Функция DOCMD

Выполняет установленную команду.
  
## <a name="syntax"></a>Синтаксис

 **DOCMD** _(commandID)_
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _commandID_ <br/> |Обязательный  <br/> |**Number** <br/> | Команда для выполнения.  <br/> |
   
## <a name="remarks"></a>Примечания

Список команд, поддерживаемых функцией DOCMD, см. в разделе "Команды DoCmd/DOCMD" в справке по автоматизации Microsoft Visio 2013 г. 
  
## <a name="example"></a>Пример

 `DOCMD (1312)`
  
Вызывает, **что диалоговое** окно Shape Data появится в пользовательском интерфейсе. 
  

