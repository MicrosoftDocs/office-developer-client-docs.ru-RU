---
title: Сведения об API репликации
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5133045a-b1e2-7728-5cd5-6d85eb940cf9
description: '���� ���������� ���������: 25 ���� 2012 �.'
ms.openlocfilehash: 532c01d6885e72753067b2d30bf2bd5f88207176
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329521"
---
# <a name="about-the-replication-api"></a>Сведения об API репликации

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
API репликации предоставляет поставщику сообщений MAPI функции синхронизации элементов Microsoft Outlook 2013 или Microsoft Outlook 2010, русская версия между сервером и частным локальным магазином на основе PST, созданным для этого поставщика. 
  
> [!NOTE]
> Поставщик хранения сообщений MAPI должен реализовать API репликации в соответствии с инструкциями в компьютере состояния [репликации.](about-the-replication-state-machine.md) Поставщик должен использовать API только в личном магазине, созданном для себя, а не в личных магазинах, созданных для других поставщиков, так как личные магазины, созданные для других поставщиков, возможно, уже создали собственные механизмы репликации на соответствующем сервере. Например, автономный файл папки (.ost) поддерживает собственные отношения репликации с сервером Microsoft Exchange. 
  
Чтобы использовать API репликации, поставщик хранения сообщений MAPI должен сначала открыть и обернуть локальный магазин на основе PST, позвонив **[в NSTServiceEntry.](nstserviceentry.md)** Затем поставщик может использовать основные интерфейсы API, **[IOSTX](iostxiunknown.md)** и **[IPSTX](ipstxiunknown.md)** для выполнения репликации. **IPSTX** предоставляется путем запроса в [IMsgStore : IMAPIProp,](imsgstoreimapiprop.md)а **IOSTX** **[предоставляется IPSTX::GetSyncObject](ipstx-getsyncobject.md)**. 
  
## <a name="the-iostx-interface"></a>Интерфейс IOSTX

Интерфейс **IOSTX** — это основной интерфейс, который выполняет синхронизацию в API репликации. **IOSTX** перемещает локальный магазин через ряд штатов, искомую информацию в каждом состоянии об изменениях в локальном магазине, а также информируя локальный магазин об изменениях на сервере. API репликации также указывает множество структур данных, которые поддерживают синхронизацию. 
  
Поставщик магазина, как клиент этого API, использует API репликации для обертывания локального магазина и перемещения по этим состояниям, нажимая изменения в локальном магазине (например, изменения в иерархии папок или добавление новых элементов) на сервер, а также получения сведений об изменениях на сервере и предоставления этих сведений **интерфейсу IOSTX.** Интерфейс **IOSTX** принимает инкрементную синхронизацию изменений (ICS), предоставляемую Microsoft Exchange Server. Дополнительные сведения о ICS см. в дополнительных сведениях о [критериях оценки ICS.](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx) С **помощью IOSTX** клиент использует ICS для мониторинга и синхронизации дополнительных изменений в иерархии или контенте локального магазина. 
  
## <a name="the-ipstx-interface"></a>Интерфейс IPSTX

 **IPSTX и** пять других интерфейсов **IPSTX *n**,* унаследованных от **IPSTX,** предоставляют дополнительные функции, которые можно использовать при выполнении репликации с помощью интерфейса **IOSTX.** Например, **[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)** позволяет заставить локальный магазин подражать диспетчеру протоколов Outlook, чтобы перенаправление исходяющих сообщений на сервер. 
  
Дополнительные сведения о переходах состояния во время репликации см. в дополнительных сведениях о машине состояния [репликации.](about-the-replication-state-machine.md)
  
## <a name="the-replication-api"></a>API репликации

API репликации содержит следующие defintions, типы данных и интерфейсы. Пример реализации поставщика магазинов для упакованных файлов личных папок (PST) см. в примере Поставщика упакованных [PST-магазинов.](about-the-sample-wrapped-pst-store-provider.md)
  
Определения
  
- [Константы для API репликации](mapi-constants.md)
    
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
    
- **[SYNCSTATE](syncstate.md)**
    
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
    

