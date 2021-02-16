---
title: TimeFromParts Function (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7f631b7e-6e3c-46dc-a05f-6a07f9a91268
description: Возвращает значение времени на основе указанных частей.
ms.openlocfilehash: 8e2105140056bc65e9af0a6eda6e40fc44caed1a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417996"
---
# <a name="timefromparts-function-access-custom-web-app"></a>TimeFromParts Function (Access custom web app)

Возвращает значение времени на основе указанных частей.
  
> [!NOTE]
> Описанная в этой статье возможность хранения данных в облаке больше не поддерживается для Office 2013 и Office 2016. Ее использование может привести к ошибке с таким сообщением: *Произошла ошибка. Не удается добавить \<службу\> из-за неполадок на сервере. Повторите попытку позже.* Чтобы получить облачное хранилище для Office Online, Office для iOS и Office для Android, ознакомьтесь с нашей программой [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Синтаксис

 **TimeFromParts** (*Hour*, *Minute*, *Second*) 
  
Функция **TimeFromParts** содержит следующие аргументы. 
  
|**Имя аргумента**|**Описание**|
|:-----|:-----|
| *Hour*  <br/> |Integer expression specifying hours.  <br/> |
| *Minute*  <br/> |Integer expression specifying minutes.  <br/> |
| *Second*  <br/> |Integer expression specifying seconds.  <br/> |
   
## <a name="see-also"></a>См. также

 **TimeFromParts** возвращает полностью инициализированное значение времени. Если аргументы недопустимы, вызывается ошибка. Если какой-либо из параметров имеет null, возвращается null. 
  

