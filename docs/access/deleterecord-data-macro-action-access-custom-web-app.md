---
title: Макрос данных макрокоманду УдалитьЗапись действие (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: f6b68a9a-e04a-476e-a407-b1779fea1953
description: Чтобы удалить запись, можно использовать УдалитьЗапись.
ms.openlocfilehash: 64742d73ec57b94474c8e27822fd3946c7673336
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806912"
---
# <a name="deleterecord-data-macro-action-access-custom-web-app"></a>Макрос данных макрокоманду УдалитьЗапись действие (приложение настраиваемых web Access)

Чтобы удалить запись, можно использовать **УдалитьЗапись** . 
  
> [!IMPORTANT]
> Корпорация Майкрософт рекомендует больше не Создание и использование веб-приложениях Access в SharePoint. Кроме того рекомендуется использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для построения без написания кода бизнес-решений для мобильных устройств и веб. 
  
## <a name="setting"></a>Параметр

**УдалитьЗапись** имеет следующие аргументы. 
  
|**Аргумент**|**Описание**|
|:-----|:-----|
|**Запись псевдонима** <br/> |Строка, идентифицирующая записи для удаления. Если аргумент *псевдоним* не указан, текущий запись удаляется.  <br/> |
   
## <a name="remarks"></a>Замечания

Локальной переменной **LastCreateRecordIdentity** можно использовать для работы с последней записи, созданной в блоке данных **СоздатьЗапись** . Например используйте следующий синтаксис для ссылки на недавно созданного записи: 
  
`[LastCreateRecordIdentity]`


