---
title: ISocialPerson IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17a2fa12-a7ef-4a95-9875-72ec6f8ceac9
description: Представляет человека в социальных сетях.
ms.openlocfilehash: d6fca18ac2d2074239bd8b435bcd40971de83670
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812727"
---
# <a name="isocialperson--iunknown"></a>ISocialPerson : IUnknown

Представляет человека в социальных сетях.
  
## <a name="members"></a>Members

В следующей таблице показаны элементы, доступные в интерфейсе **ISocialPerson** . 
  
|**Имя**|**Тип участника**|**Описание**|
|:-----|:-----|:-----|
|[GetActivities](isocialperson-getactivities.md) <br/> |Метод  <br/> |Этот метод устарел и начиная с Outlook Social Connector 2013.  <br/> |
|[GetDetails](isocialperson-getdetails.md) <br/> |Метод  <br/> |Получает строку, представляющую сведений для пользователя, такие как имя, Фамилия и URL-адрес изображения профилей.  <br/> |
|[GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) <br/> |Метод  <br/> |Получает строку, представляющую коллекцию людей.  <br/> |
|[GetFriendsAndColleaguesIDs](isocialperson-getfriendsandcolleaguesids.md) <br/> |Метод  <br/> |Этот метод в настоящее время не поддерживается.  <br/> |
|[GetPicture](isocialperson-getpicture.md) <br/> |Метод  <br/> |Получает массив байтов, который содержит изображение ресурсов для пользователя.  <br/> |
|[GetStatus](isocialperson-getstatus.md) <br/> |Метод  <br/> |Этот метод в настоящее время не поддерживается.  <br/> |
   
## <a name="remarks"></a>Замечания

Поставщика Outlook Social Connector (OSC) необходимо реализовать этот интерфейс для взаимодействия с OSC.
  
## <a name="see-also"></a>См. также

- [Интерфейсы поставщика Outlook Social Connector](outlook-social-connector-provider-interfaces.md)

