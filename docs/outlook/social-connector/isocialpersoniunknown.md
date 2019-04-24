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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331943"
---
# <a name="isocialperson--iunknown"></a>ISocialPerson : IUnknown

Представляет пользователя в социальной сети.
  
## <a name="members"></a>Members

В следующей таблице показаны элементы, доступные в интерфейсе **исоЦиалперсон** . 
  
|**Name**|**Тип элемента**|**Описание**|
|:-----|:-----|:-----|
|[Операции с действиями](isocialperson-getactivities.md) <br/> |Метод  <br/> |Этот метод является устаревшим, так как Outlook Social Connector 2013.  <br/> |
|[Подробные сведения](isocialperson-getdetails.md) <br/> |Метод  <br/> |Получает строку, представляющую сведения о пользователе, такие как имя, фамилию и URL-адрес изображения профиля.  <br/> |
|[Жетфриендсандколлеагуес](isocialperson-getfriendsandcolleagues.md) <br/> |Метод  <br/> |Получает строку, представляющую коллекцию людей.  <br/> |
|[Жетфриендсандколлеагуесидс](isocialperson-getfriendsandcolleaguesids.md) <br/> |Метод  <br/> |В настоящее время этот метод не поддерживается.  <br/> |
|[GetPicture](isocialperson-getpicture.md) <br/> |Метод  <br/> |Возвращает массив байтов, который содержит ресурс изображения для пользователя.  <br/> |
|[GetStatus](isocialperson-getstatus.md) <br/> |Метод  <br/> |В настоящее время этот метод не поддерживается.  <br/> |
   
## <a name="remarks"></a>Комментарии

Поставщик Outlook Social Connector (OSC) должен реализовать этот интерфейс для взаимодействия с OSC.
  
## <a name="see-also"></a>См. также

- [Интерфейсы поставщика социальных соединителей Outlook](outlook-social-connector-provider-interfaces.md)

