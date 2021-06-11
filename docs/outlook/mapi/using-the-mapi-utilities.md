---
title: Использование утилит MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5f0e5c97-5089-47cb-b604-2292b2ff945c
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: d8ec18ee7b80d8603266cf827f9484ee85bdb03c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409988"
---
# <a name="using-the-mapi-utilities"></a>Использование утилит MAPI

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Утилиты MAPI состоит из объектов данных таблицы и данных свойств и различных функций для поддержки различных функций. Клиент может нуждаться только в этих утилитах и не должен войти в подсистему MAPI, чтобы установить связь с поставщиками услуг. Если клиент подходит к этой категории, позвоните в функцию API [ScInitMapiUtil,](scinitmapiutil.md) а не на [функцию MAPIInitialize](mapiinitialize.md) во время инициализации. 
  
 **ScInitMapiUtil** позволяет клиентам использовать функции утилиты, для которых требуются аллигаторы MAPI, но которые явно не требуют их. Когда пришло время закрыться, позвоните [DeinitMapiUtil,](deinitmapiutil.md) чтобы освободить ресурсы, а [не MAPIUninitialize](mapiuninitialize.md). Клиенты, которые никогда не называют **MAPIInitialize,** не должны вызывать **MAPIUninitialize.**
  
Если вы вызвали **ScInitMapiUtil,** а не **MAPIInitialize** и используете таблицы с помощью методов **ITableData,** а не методов **IMAPITable,** знайте, что уведомления таблицы не будут работать. Уведомления требуют использования библиотек MAPI и [IMAPITable: IUnknown](imapitableiunknown.md).
  

