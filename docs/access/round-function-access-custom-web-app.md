---
title: Round Function (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4af7fbe2-ee34-4a52-b55e-ce3983313b5e
description: Возвращает числовую величину с закругленным или усеченным значением по указанной длине или точности.
ms.openlocfilehash: 0afab8c3434aef58c4bb25aee22eefd95732797b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413747"
---
# <a name="round-function-access-custom-web-app"></a>Round Function (Access custom web app)

Возвращает числовую величину с закругленным или усеченным значением по указанной длине или точности.
  
> [!IMPORTANT]
> Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint. В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств. 
  
## <a name="syntax"></a>Синтаксис

 **Round** (*Number*, *Precision*  , [  *TruncateInsteadOfRound*  ]) 
  
Функция **Round** содержит следующие аргументы. 
  
|**Имя аргумента**|**Описание**|
|:-----|:-----|
| *Number*  <br/> |Числовое выражение.  <br/> |
| *Точность*  <br/> |Точность  *округлимого*  числа.  *Точность*  должна быть числом выражения. Если  *точность*  — положительное число,  *число*  округляется до числа десятичных позиций, заданных по длине. Если *точность* является отрицательным числом,  число округляется в левой части десятичной точки, как указано по длине.  <br/> |
| *TruncateInsteadOfRound*  <br/> |Тип выполняемой операции. Если опущен или установлено 0,  *число*  округлится. Если задано значение, не большее 0,  *число*  усечено. Значение по умолчанию равно 0.  <br/> |
   
## <a name="remarks"></a>Примечания

 **Округл** всегда возвращает значение. Если длина отрицательной и превышает число цифр до десятичной точки, **Round** возвращает 0. 
  

