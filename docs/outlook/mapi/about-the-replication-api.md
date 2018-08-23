---
title: Сведения об API репликации
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5133045a-b1e2-7728-5cd5-6d85eb940cf9
description: '���� ���������� ���������: 25 ���� 2012 �.'
ms.openlocfilehash: 272d4147d60df53ef30a668faa8abe89f96cd654
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582324"
---
# <a name="about-the-replication-api"></a>Сведения об API репликации

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Интерфейс API репликации предоставляет функциональные возможности для поставщика хранилища сообщений MAPI для синхронизации элементов Microsoft Outlook 2013 или Microsoft Outlook 2010 между сервером и закрытый на основе .pst локального хранилища, созданный для этого поставщика. 
  
> [!NOTE]
> Поставщик хранения сообщений MAPI необходимо реализовать API репликации согласно инструкциям в [О конечного автомата репликации](about-the-replication-state-machine.md). Поставщик должен использовать API-Интерфейс только на личном хранилище, созданные для самого, а не на личные хранилища, созданные для других поставщиков, так как для создания личных хранилищ других поставщиков уже настроить собственные механизма репликации с соответствующими сервером. Например файл автономной папки (OST) поддерживает собственный репликации отношения с Microsoft Exchange server. 
  
Чтобы использовать API репликации, поставщика хранилища сообщений MAPI сначала необходимо открыть и перенос локального хранилища на основе .pst путем вызова **[NSTServiceEntry](nstserviceentry.md)**. Поставщик затем можно использовать основные интерфейсы API, **[IOSTX](iostxiunknown.md)** и **[IPSTX](ipstxiunknown.md)**, чтобы выполнить репликацию. **IPSTX** предоставляется с помощью запроса на [IMsgStore: IMAPIProp](imsgstoreimapiprop.md), и **IOSTX** обеспечивается **[IPSTX::GetSyncObject](ipstx-getsyncobject.md)**. 
  
## <a name="the-iostx-interface"></a>Интерфейс IOSTX

Интерфейс **IOSTX** — это основной интерфейс, который выполняет синхронизацию в API репликации. **IOSTX** перемещает локального хранилища ряд состояний, получение сведений об изменениях в локальном хранилище каждого состояния, а также о том, локального хранилища изменения на сервере. API репликации также приведены несколько структур данных, которые поддерживают синхронизацию. 
  
Поставщик хранения, как клиент этот интерфейс API использует API репликации для переноса локального хранилища и перемещаться по эти состояния принудительную изменений в локальном хранилище (например, изменения иерархии папок или добавление новых элементов) на сервер, а также извлечение сведения об изменениях на сервере и предоставляя эти сведения об интерфейсе **IOSTX** . Интерфейс **IOSTX** принимает добавочные изменения синхронизации (ICS) предоставлено Microsoft Exchange Server. Дополнительные сведения о ICS [Критерии оценки ICS](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx)см. Через **IOSTX**клиент использует ICS для мониторинга и синхронизировать добавочные изменения иерархии или контента для локального хранилища. 
  
## <a name="the-ipstx-interface"></a>Интерфейс IPSTX

 **IPSTX** и пять других ** IPSTX *n* ** интерфейсы, производные от **IPSTX** предоставляют функциональные возможности модуля поддержки, который можно использовать при выполнении репликации с помощью интерфейса **IOSTX** . Например **[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)** позволяет сделать локального хранилища эмуляции диспетчера протокола Outlook очереди исходящих сообщений на сервере. 
  
Дополнительные сведения о переходы между состояниями во время репликации можно [О конечного автомата репликации](about-the-replication-state-machine.md).
  
## <a name="the-replication-api"></a>Интерфейс API репликации

API репликации предоставляет файлов определения, типы данных и интерфейсы. Пример реализации поставщика хранилища для оболочку файлы личных папок (PST) в разделе [О пример оболочку PST поставщика хранилища](about-the-sample-wrapped-pst-store-provider.md).
  
Определения:
  
- [Константы для репликации API](mapi-constants.md)
    
Функции:
  
- **[NSTServiceEntry](nstserviceentry.md)**
    
Типы данных:
  
- **[DNHIER](dnhier.md)**
    
- **[DNTBL](dntbl.md)**
    
- **[DNTBLE](dntble.md)**
    
- **[FEID](feid.md)**
    
- **[HDRSYNC](hdrsync.md)**
    
- **[LTID](ltid.md)**
    
- **[MEID](meid.md)**
    
- **[OLFI](olfi.md)**
    
- **[SKEY](skey.md)**
    
- **[SYNC](sync.md)**
    
- **[SYNCCONT](synccont.md)**
    
- **[СОСТОЯНИЕ](syncstate.md)**
    
- **[UPDEL](updel.md)**
    
- **[UPDELE](updele.md)**
    
- **[UPFLD](upfld.md)**
    
- **[UPHIER](uphier.md)**
    
- **[UPMOV](upmov.md)**
    
- **[UPMSG](upmsg.md)**
    
- **[UPREAD](upread.md)**
    
- **[UPREADE](upreade.md)**
    
- **[UPTBL](uptbl.md)**
    
- **[UPTBLE](uptble.md)**
    
Интерфейсы:
  
- **[IOSTX](iostxiunknown.md)**
    
- **[IPSTX](ipstxiunknown.md)**
    
- **[IPSTX2](ipstx2ipstx.md)**
    
- **[IPSTX3](ipstx3ipstx2.md)**
    
- **[IPSTX4](ipstx4ipstx3.md)**
    
- **[IPSTX5](ipstx5ipstx4.md)**
    
- **[IPSTX6](ipstx6ipstx5.md)**
    

