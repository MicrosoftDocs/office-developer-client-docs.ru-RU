---
title: Инициализация OLE для MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 53b65299-69f8-4fc0-8d9b-f666e814aaac
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: cd279c17574ce73b42d5e07e96ac817af71dc700
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589807"
---
# <a name="initializing-ole-for-mapi"></a>Инициализация OLE для MAPI

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
При использовании OLE, вызовите функцию OLE [OleInitialize](http://msdn.microsoft.com/en-us/library/ms690134%28v=VS.85%29.aspx) для инициализации библиотеки OLE. **OleInitialize** инициализирует глобальные данные для сеанса и подготавливает библиотек OLE для приема звонков. Сведения о вызовах **OleInitialize**просмотрите пакет SDK для Windows.
  

