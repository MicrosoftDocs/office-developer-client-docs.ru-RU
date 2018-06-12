---
title: PROP_ACCT_SENTITEMS_EID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f199a97f-55d6-9297-adc4-e9f7b4b5f58b
description: Представляет идентификатор записи папки по умолчанию для отправленных элементов для учетной записи.
ms.openlocfilehash: 7795e8a112f0575b764fd55e92d27c7085e3d3a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807936"
---
# <a name="propacctsentitemseid"></a>PROP_ACCT_SENTITEMS_EID

Представляет идентификатор записи папки по умолчанию для отправленных элементов для учетной записи. 
  
## <a name="quick-info"></a>Краткие сведения

В разделе [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Идентификатор:  <br/> |0x0020  <br/> |
|Тип свойства:  <br/> |PT_BINARY  <br/> |
|Свойство tag:  <br/> |0x00200102  <br/> |
|Access:  <br/> |Только для чтения  <br/> |
   
## <a name="remarks"></a>Замечания

Получение этого свойства с помощью [IOlkAccount::GetProp](iolkaccount-getprop.md).
  
Папка по умолчанию для отправленных элементов — **Отправленные**.
  
Это свойство доступно только для чтения учетных записей POP3 и IMAP. При попытке установить это свойство для следующих типов учетных записей возвращает **E_ACCT_NOT_FOUND**. 
  

