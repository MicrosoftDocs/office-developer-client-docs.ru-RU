---
title: ISocialPerson IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17a2fa12-a7ef-4a95-9875-72ec6f8ceac9
description: Представляет человека в социальной сети.
ms.openlocfilehash: 0ad129b0fc15fc9f3ccdf1cff7d8519bb07b024e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407013"
---
# <a name="isocialperson--iunknown"></a>ISocialPerson : IUnknown

Представляет человека в социальной сети.
  
## <a name="members"></a>"Участники"

В следующей таблице показаны участники, доступные в **интерфейсе ISocialPerson.** 
  
|**Имя**|**Тип участника**|**Описание**|
|:-----|:-----|:-----|
|[GetActivities](isocialperson-getactivities.md) <br/> |Метод  <br/> |Этот метод был обесценив с Outlook Social Connector 2013.  <br/> |
|[GetDetails](isocialperson-getdetails.md) <br/> |Метод  <br/> |Получает строку, которая представляет сведения для пользователя, например имя, фамилию и URL-адрес к изображению профиля.  <br/> |
|[GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) <br/> |Метод  <br/> |Получает строку, представляюную коллекцию людей.  <br/> |
|[GetFriendsAndColleaguesIDs](isocialperson-getfriendsandcolleaguesids.md) <br/> |Метод  <br/> |Этот метод в настоящее время не поддерживается.  <br/> |
|[GetPicture](isocialperson-getpicture.md) <br/> |Метод  <br/> |Получает массив bytes, который содержит ресурс изображения для человека.  <br/> |
|[GetStatus](isocialperson-getstatus.md) <br/> |Метод  <br/> |Этот метод в настоящее время не поддерживается.  <br/> |
   
## <a name="remarks"></a>Примечания

Поставщик Outlook social Connector (OSC) должен реализовать этот интерфейс для связи с OSC.
  
## <a name="see-also"></a>См. также

- [Outlook Интерфейсы поставщиков социальных соединители](outlook-social-connector-provider-interfaces.md)

