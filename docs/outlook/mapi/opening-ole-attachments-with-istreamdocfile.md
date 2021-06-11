---
title: Открытие вложений OLE с помощью IStreamDocfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f91df63c-ff6d-4c63-a665-5bcfdabe7e0e
description: 'Последнее изменение: 06 июля 2012 г.'
ms.openlocfilehash: 2de13be34e8d81f88bfba872dda6e5534eb431bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326231"
---
# <a name="opening-ole-attachments-with-istreamdocfile"></a>Открытие вложений OLE с помощью IStreamDocfile

**Область применения**: Outlook 2013 | Outlook 2016 
  
При открытии вложения объекта OLE используйте **интерфейс IStreamDocfile,** а не [IStream](https://msdn.microsoft.com/library/windows/desktop/aa380034%28v=vs.85%29.aspx) или [IStorage.](https://msdn.microsoft.com/library/windows/desktop/aa380015%28v=vs.85%29.aspx) 

**IStreamDocfile** предоставляет прямой доступ к объекту с помощью структурированного хранилища, устраняя необходимость выполнения операции копирования и уменьшая накладные расходы. **IStreamDocfile** — это специфическая реализация **IStream** с контентом потока, гарантированно отформатированный в виде структурированного хранилища. **IStreamDocfile** реализуется поставщиками магазинов сообщений. 
  

