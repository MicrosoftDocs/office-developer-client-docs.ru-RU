---
title: ИсоЦиалперсон IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17a2fa12-a7ef-4a95-9875-72ec6f8ceac9
description: Представляет пользователя в социальной сети.
ms.openlocfilehash: 0ad129b0fc15fc9f3ccdf1cff7d8519bb07b024e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407013"
---
# <a name="isocialperson--iunknown"></a>ISocialPerson : IUnknown

Представляет пользователя в социальной сети.
  
## <a name="members"></a>"Участники"

В следующей таблице показаны элементы, доступные в интерфейсе **исоЦиалперсон** . 
  
|**имя**|**Тип элемента**|**Описание**|
|:-----|:-----|:-----|
|[Операции с действиями](isocialperson-getactivities.md) <br/> |Method  <br/> |Этот метод является устаревшим, так как Outlook Social Connector 2013.  <br/> |
|[Подробные сведения](isocialperson-getdetails.md) <br/> |Method  <br/> |Получает строку, представляющую сведения о пользователе, такие как имя, фамилию и URL-адрес изображения профиля.  <br/> |
|[жетфриендсандколлеагуес](isocialperson-getfriendsandcolleagues.md) <br/> |Method  <br/> |Получает строку, представляющую коллекцию людей.  <br/> |
|[жетфриендсандколлеагуесидс](isocialperson-getfriendsandcolleaguesids.md) <br/> |Method  <br/> |В настоящее время этот метод не поддерживается.  <br/> |
|[GetPicture](isocialperson-getpicture.md) <br/> |Method  <br/> |Возвращает массив байтов, который содержит ресурс изображения для пользователя.  <br/> |
|[GetStatus](isocialperson-getstatus.md) <br/> |Method  <br/> |В настоящее время этот метод не поддерживается.  <br/> |
   
## <a name="remarks"></a>Примечания

Поставщик Outlook Social Connector (OSC) должен реализовать этот интерфейс для взаимодействия с OSC.
  
## <a name="see-also"></a>См. также

- [Интерфейсы поставщика социальных соединителей Outlook](outlook-social-connector-provider-interfaces.md)

