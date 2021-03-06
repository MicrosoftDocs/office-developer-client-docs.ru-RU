---
title: Возможности, не поддерживаемые диспетчерами форм
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b51e9e03-a333-4fdc-b6fe-87bd4e947b9f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: e31eacaae54968fbdbd9fe0345130a8d09c3509f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419382"
---
# <a name="capabilities-not-supported-by-form-managers"></a>Возможности, не поддерживаемые диспетчерами форм

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Следующие функции не поддерживаются менеджером форм по умолчанию из соображений производительности, но могут быть поддержаны настраиваемые менеджеры форм.
  
- Иерархия, которая позволяет сгруппированы или классифицируются формы в библиотеке форм. Библиотека форм — это база данных форм с плоским файлом.
    
- Управление доступом для категорий форм, соответствующих классам сообщений или суперклассам.
    
- Поддержка нескольких языковых версий одной формы в одной библиотеке форм.
    
Это проблемы реализации. Нет ничего, чтобы предотвратить реализацию этих функций настраиваемой диспетчером форм.
  
Архитектура форм MAPI не поддерживает одновременное управление несколькими руководителями форм. Хотя MAPI поддерживает несколько одновременно поставщиков, поставщиков транспортных сообщений и поставщиков адресных книг, поддерживается только один диспетчер форм.
  
Так как одновременно может выполняться только один диспетчер форм, если вы реализуете настраиваемый диспетчер форм, вам придется повторно реализовать все функции из нужного по умолчанию администратора форм. Так как настраиваемый диспетчер форм полностью заменит диспетчер форм по умолчанию, возможности диспетчера форм по умолчанию будут недоступны, если они не будут дублироваться в настраиваемом диспетчере форм.
  
## <a name="see-also"></a>См. также



[Формы MAPI](mapi-forms.md)

