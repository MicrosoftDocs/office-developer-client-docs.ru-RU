---
title: PROP_ACCT_SENTITEMS_EID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f199a97f-55d6-9297-adc4-e9f7b4b5f58b
description: Представляет идентификатор папки по умолчанию для отправленных элементов для учетной записи.
ms.openlocfilehash: 24bb4714a4f4964ac3d84ea7a792e64da67599df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431843"
---
# <a name="propacctsentitemseid"></a>PROP_ACCT_SENTITEMS_EID

Представляет идентификатор папки по умолчанию для отправленных элементов для учетной записи. 
  
## <a name="quick-info"></a>Краткие сведения

Обратитесь к разделу [иолкаккаунт](iolkaccount.md).
  
|||
|:-----|:-----|
|Идентификатор:  <br/> |0x0020  <br/> |
|Тип свойства:  <br/> |PT_BINARY  <br/> |
|Тег свойства:  <br/> |0x00200102  <br/> |
|Обращения  <br/> |Только для чтения  <br/> |
   
## <a name="remarks"></a>Примечания

Получить это свойство можно с помощью [иолкаккаунт::/Prop](iolkaccount-getprop.md).
  
Папкой по умолчанию для отправленных элементов отПравляются **элементы**.
  
Это свойство доступно только для чтения для учетных записей POP3 и IMAP. При попытке установить это свойство для этих типов учетных записей возвращается **е_аккт_нот_фаунд**. 
  

