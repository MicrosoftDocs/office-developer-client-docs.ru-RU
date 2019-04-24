---
title: Настройка службы сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d68892e3-7c87-4b3a-a691-bff92f83ed00
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 4c3d30c7111e7b26886cbfb069ec2822d2ee0234
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335114"
---
# <a name="configuring-a-message-service"></a>Настройка службы сообщений

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
 **Настройка всех поставщиков служб в службе сообщений**
  
- Call [имсгсервицеадмин:: конфигуремсгсервице](imsgserviceadmin-configuremsgservice.md). Если все данные, необходимые для настройки, доступны программно, вы можете выбрать, следует ли отображать пользовательский интерфейс. Тем не менее, если некоторые сведения для одного или нескольких поставщиков недоступны, убедитесь, что установлен флаг СЕРВИЦЕ_УИ_АЛЛОВЕД или СЕРВИЦЕ_УИ_АЛВАЙС. Запрет доступа к пользовательскому интерфейсу при недоступности необходимых данных конфигурации приводит к ненастроенной службе сообщений.
    
 **Настройка одного поставщика услуг в службе сообщений**
  
1. Call [IMAPISession:: жетстатустабле](imapisession-getstatustable.md) для доступа к объекту Status поставщика услуг. 
    
2. Call [имапистатус:: сеттингсдиалог](imapistatus-settingsdialog.md) для отображения страницы свойств поставщика услуг. 
    
Дополнительные сведения об использовании объектов Status приведены в статье [Status Table and Status Objects](status-table-and-status-objects.md).
  

