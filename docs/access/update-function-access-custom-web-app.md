---
title: Update Function (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8a8c52c9-81b9-4d10-b42b-e360c67bcf4e
description: Возвращает, была ли предпринята попытка операции INSERT или UPDATE в указанном поле.
ms.openlocfilehash: 20e1b87be857f302f36244a6733625dc477da912
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410919"
---
# <a name="update-function-access-custom-web-app"></a>Update Function (Access custom web app)

Возвращает, была ли предпринята попытка операции INSERT или UPDATE в указанном поле.
  
> [!NOTE]
> Описанная в этой статье возможность хранения данных в облаке больше не поддерживается для Office 2013 и Office 2016. Ее использование может привести к ошибке с таким сообщением: *Произошла ошибка. Не удается добавить \<службу\> из-за неполадок на сервере. Повторите попытку позже.* Чтобы получить облачное хранилище для Office Online, Office для iOS и Office для Android, ознакомьтесь с нашей программой [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Синтаксис

 **Обновление** *(столбец)* 
  
Функция **Update** содержит следующие аргументы. 
  
|**Имя аргумента**|**Описание**|
|:-----|:-----|
| *Столбец*  <br/> |Имя поля для проверки операции INSERT или UPDATE.  <br/> |
   
## <a name="remarks"></a>Примечания

Функция **Update** возвращает true независимо от того, была ли попытка INSERT или UPDATE успешной. 
  

