---
title: Функция рэнд (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6390b325-025e-4546-bb19-1cd1c45ceb5a
description: Возвращает псевдослучайное число от 0 до 1.
ms.openlocfilehash: ed0f9991b2b1d9553d6d45524d6b1e4e5321ea7e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807095"
---
# <a name="rand-function-access-custom-web-app"></a>Функция рэнд (приложение настраиваемых web Access)

Возвращает псевдослучайное число от 0 до 1.
  
> [!IMPORTANT]
> Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint. В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств. 
  
## <a name="syntax"></a>Синтаксис

 **Рэнд** ([ *Начального значения* ]) 
  
Функция **рэнд** содержит следующий аргумент. 
  
|**Имя аргумента**|**Описание**|
|:-----|:-----|
| *Seed*  <br/> |Целочисленное выражение, которое задает начальное значение. Если *Начальное* значение не указано, начальное значение назначается в произвольном порядке.  <br/> |
   
## <a name="remarks"></a>Замечания

Повторные вызовы функции **рэнд** с того же начального значения возвращает одинаковые результаты. 
  

