---
title: Функция RUNMACRO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033809
localization_priority: Normal
ms.assetid: 86b0f071-5e0b-56de-ff5b-63c114ad823a
description: Вызывает макрос в проекте Microsoft Visual Basic для приложений (VBA).
ms.openlocfilehash: 77045bd67fe9be9aab14e73199b33b93c6d70c2c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428090"
---
# <a name="runmacro-function"></a>Функция RUNMACRO

Вызывает макрос в проекте Microsoft Visual Basic для приложений (VBA). 
  
## <a name="syntax"></a>Синтаксис

RUNMACRO (** *macroname* ** [, ** *projname_opt* ** ]) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _macroname_ <br/> |Обязательный  <br/> |**String** <br/> |Имя вызываемого макроса.  <br/> |
| _projname_opt_ <br/> |Необязательный  <br/> |**String** <br/> | Проект, содержащий макрос.  <br/> |
   
## <a name="remarks"></a>Примечания

Если проект указан, корпорация Майкрософт Visio все открытые документы для  одного из projname_opt  и вызывает макрона в этом проекте. Если _projname_opt_ опущен или null (""),  предполагается, что макрона будет в проекте VBA документа, который содержит оцениваемую формулу RUNMACRO. 
  
Функция RUNMACRO отличается от функции CALLTHIS тем, что она не передает ссылку на форму, которая владеет формулой, оцениваемой в _макронам._ Как и CALLTHIS, функция RUNMACRO не требует ссылки на projname_opt  _вызов_ в нее. 
  
 Код VBA, который вызывается, когда экземпляр Visio оценивает функцию RUNMACRO в формуле, не должен закрывать документ, содержащий ячейку с помощью функции, так как результат ошибки приложения и Visio заканчивается. 
  
Если необходимо закрыть документ, содержащий ячейку, использующую функцию RUNMACRO, используйте один из следующих методов:
  
- Закрой документ из кода, который не является VBA.
    
- Закрой документ из проекта, кроме закрываемого.
    
- Вывешить сообщения о окне, чтобы закрыть окна в документе, а не закрыть документ.
    
Дополнительные сведения о запуске кода в Visio [Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) см. в этой ссылке ShapeSheet. 
  
## <a name="example"></a>Пример

В следующем примере вызывается макрос MyTest в модуле класса ThisDocument проекта VBA, содержащего формулу RUNMACRO. 
  
RUNMACRO ("ThisDocument.MyTest") 
  

