---
title: Работа со свойствами при помощи таблицы
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c18ed9f7-c053-4453-b0b1-06234cdfb025
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: e4e7ecda40f3f3fcb05700ba3e8b79ab21cbe35b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812566"
---
# <a name="using-a-table-to-work-with-properties"></a>Работа со свойствами при помощи таблицы

  
  
**Относится к**: Outlook 
  
Многие свойства доступны из объектов, которые поддерживают их и как столбцы в таблицах. По возможности получения этих свойств с помощью таблицы.
  
Вызов [IMAPITable::SetColumns](imapitable-setcolumns.md) для включения всех свойств, которые ваш клиент должен и [IMAPITable::QueryRows](imapitable-queryrows.md) получить все строки в таблице. 
  
Эти два звонка обычно подходят для извлечения достаточно сведений для отображения пользователю и часто достаточно для любые необходимые внутренней обработки вызовов **OpenEntry** для открытия ненужных объектов. 
  
Существует только два исключения:
  
- Если свойство не более 255 байт. ** IMAPITable ** интерфейса не может возвращать значение свойства всей, вместо этого усечение до 255 байт. Тем не менее подумайте о задать это соотношение. При отображении эти данные для пользователя, 255 байт может быть достаточно для текстовых полей, например комментария. 
    
- Если вам требуется определенное свойство из одной строки в таблице. В этом случае не требуется для создания таблицы с помощью свойства, которые никогда не должны использоваться. В большинстве случаев потребуется те же свойства для всех строк.
    
