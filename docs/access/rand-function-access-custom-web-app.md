---
title: Rand Function (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6390b325-025e-4546-bb19-1cd1c45ceb5a
description: Возвращает псевдо-случайный номер между 0 и 1.
ms.openlocfilehash: 02d914de9d74083a6ebf76f6d0e556fe51954a24
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416610"
---
# <a name="rand-function-access-custom-web-app"></a>Rand Function (Access custom web app)

Возвращает псевдо-случайный номер между 0 и 1.
  
> [!IMPORTANT]
> Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint. В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств. 
  
## <a name="syntax"></a>Синтаксис

 **Rand** ( [  *Seed*  ]) 
  
Функция **Rand** содержит следующий аргумент. 
  
|**Имя аргумента**|**Описание**|
|:-----|:-----|
| *Seed*  <br/> |Integer expression that gives the seed value. Если  *seed*  не указан, значение семени задано случайным образом.  <br/> |
   
## <a name="remarks"></a>Примечания

Повторяющиеся вызовы **функции Rand** с одним и тем же семенем возвращают те же результаты. 
  

