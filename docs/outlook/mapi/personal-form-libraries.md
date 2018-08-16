---
title: Личные библиотеки форм
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ffcd93c-3737-4342-9cd0-2ca7c0fba52c
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 0793fefd744eecc95899c4166cb8a1a6a2e6cd2f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810097"
---
# <a name="personal-form-libraries"></a>Личные библиотеки форм

  
  
**Относится к**: Outlook 
  
Как названия, библиотек личных форм содержат формы представлять интерес для определенного пользователя. Библиотека личных форм пользователя — это библиотека форм, связанные с хранилищем сообщений по умолчанию, определенный в профиле пользователя; Каждый профиль, установленные на рабочей станции можно использовать хранилища отдельные по умолчанию и, следовательно, библиотеки форм отдельные личные. Библиотека личных форм может содержать копии форм, которые также содержатся в других библиотеках форм в дополнение к другим форм.
  
Библиотека личных форм реализована в таблице связанного содержимого в корневой папке в хранилище сообщений по умолчанию пользователя, будет ли, который находится на сервере или локально на рабочей станции пользователя, не имеет значения. Если хранилище сообщений по умолчанию хранится на рабочей станции пользователя, личных форм библиотекам предлагают повышения производительности, который позволяет приложениям для доступа к формам локально вместо предложенного по сети. Он также предоставляет форм пользователям доступ работа в автономном режиме, может произойти, если пользователи хотят иметь свои формы с ними на портативные компьютеры и без доступа к сети.
  
Свойства и базовой реализацией записи Библиотека личных форм включают свойство «Контейнер ID», который определяет основной контейнер, локальной записи должны быть синхронизированы с. Это может быть идентификатор произвольной папке, которая содержит формы. Эта функция особенно полезна, если вы используете Диспетчер настраиваемой формы, который поддерживает какую-либо библиотека форм всей организации; Диспетчер форм будет взяла на себя синхронизация форм, хранимые в библиотеке личных форм и библиотека форм всей организации. Произойдет, вероятно, когда диспетчер форм был загружен, но теоретически может произойти в любое время.
  
## <a name="see-also"></a>См. также



[Формы MAPI](mapi-forms.md)
