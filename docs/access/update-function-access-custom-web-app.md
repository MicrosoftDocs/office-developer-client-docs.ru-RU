---
title: Функция Update (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8a8c52c9-81b9-4d10-b42b-e360c67bcf4e
description: Возвращает значение, указывающее, была ли предпринята попытка выполнить операцию INSERT или UPDATE для указанного поля.
ms.openlocfilehash: 20e1b87be857f302f36244a6733625dc477da912
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307828"
---
# <a name="update-function-access-custom-web-app"></a>Функция Update (пользовательское веб-приложение для Access)

Возвращает значение, указывающее, была ли предпринята попытка выполнить операцию INSERT или UPDATE для указанного поля.
  
> [!NOTE]
> Описанная в этой статье возможность хранения данных в облаке больше не поддерживается для Office 2013 и Office 2016. Ее использование может привести к ошибке с таким сообщением: *Произошла ошибка. Не удается добавить \<службу\> из-за неполадок на сервере. Повторите попытку позже.* Чтобы получить облачное хранилище для Office Online, Office для iOS и Office для Android, ознакомьтесь с нашей программой [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Синтаксис

 **Обновление** (*Столбец*) 
  
Функция **Update** содержит указанные ниже аргументы. 
  
|**Имя аргумента**|**Описание**|
|:-----|:-----|
| *Column*  <br/> |Имя поля, для которого проверяется операция вставки или обновления.  <br/> |
   
## <a name="remarks"></a>Замечания

Функция **Update** ВОЗВРАЩАЕТ значение true независимо от того, успешно ли выполнена попытка вставки или обновления. 
  

