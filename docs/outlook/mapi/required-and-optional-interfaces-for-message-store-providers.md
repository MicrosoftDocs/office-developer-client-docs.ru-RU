---
title: Обязательные и необязательные интерфейсы для поставщиков хранилища сообщений
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc62e57e-82a4-4f37-8d1b-7cdf828b951e
description: '���� ���������� ���������: 7 ������� 2015 �.'
ms.openlocfilehash: d8cd03fa184865446da48d7532764ba71e0e47d4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812123"
---
# <a name="required-and-optional-interfaces-for-message-store-providers"></a>Обязательные и необязательные интерфейсы для поставщиков хранилища сообщений

 
  
**Применимо к**: Outlook 
  
MAPI определяет набор интерфейсов, которые относятся к поставщиков хранилища сообщений. Из-за широкий спектр возможностей, которые можно выбрать хранилищем сообщений для реализации некоторых из этих интерфейсов являются обязательными и — нет. В следующей таблице перечислены интерфейсы MAPI, которые связаны с поставщиков хранилища сообщений, указывает обязательный или необязательный интерфейсы и описывает их назначение.
  
|**Интерфейс**|**Состояние**|**Описание**|
|:-----|:-----|:-----|
|[IMSProvider](imsprovideriunknown.md) <br/> |Обязательный  <br/> |Регистрация или из хранилища сообщений.  <br/> |
|[IMSLogon](imslogoniunknown.md) <br/> |Обязательный  <br/> |Открывает папок или сообщений, проверяет идентификатор хранилища сообщений и обрабатывает уведомления.  <br/> |
|[IMsgStore](imsgstoreimapiprop.md) <br/> |Обязательный  <br/> |Открытие папки или сообщения, находит специальные папки и обработки сообщений, отправляемых.  <br/> |
|[IMAPIFolder](imapifolderimapicontainer.md) <br/> |Обязательный  <br/> |Поиск и обработка сообщений и вложенных папок.  <br/> |
|[IMessage](imessageimapiprop.md) <br/> |Обязательный  <br/> |Управляет вложения и задает некоторые свойства сообщения.  <br/> |
|[IMAPITable](imapitableiunknown.md) <br/> |Обязательный  <br/> |Позволяет другим объектам для представления коллекции данных в различные компоненты MAPI.  <br/> |
|[IMAPIStatus](imapistatusimapiprop.md) <br/> |Обязательный  <br/> |Позволяет клиентам для проверки состояния хранилища сообщений и для выполнения некоторых задач конфигурации.  <br/> |
|[IAttach](iattachimapiprop.md) <br/> |Optional  <br/> |Доступ к вложения свойства сообщений, если поставщик хранения поддерживает вложенных файлов.  <br/> |
|**IStorage** <br/> |Optional  <br/> |Управляет структурированных объектов хранилища, если поставщик хранения поддерживает вложения объекта OLE.  <br/> |
|**IStream** <br/> |Optional  <br/> |Позволяет объектов сообщений и вложений для чтения и записи данных в поток объекты.  <br/> |
|**IStreamDocfile** <br/> |Optional  <br/> |Включение некоторых поставщиков услуг для открытия объекта хранилища, например составной файл в формате OLE 2.0.  <br/> |
   
Основные сведения, необходимые для реализации **IMAPIFolder**, **IMessage**, **IMAPIStatus**и **IMAPITable** описана в разделы справочника по для этих интерфейсов. В этом разделе содержатся дополнительные сведения, которые более непосредственно связан с поставщиков хранилища сообщений. Rest интерфейсы MAPI должен быть реализован в соответствии с сведения в этом разделе и в соответствующие ссылки на разделы. Обратитесь к разделу COM и службы объект ActiveX в пакете SDK Windows Дополнительные сведения о реализации **IStorage** **IStream**и **IStreamDocFile**.
  
## <a name="see-also"></a>См. также



[���������� ���������� ��������� ��������� MAPI](developing-a-mapi-message-store-provider.md)
