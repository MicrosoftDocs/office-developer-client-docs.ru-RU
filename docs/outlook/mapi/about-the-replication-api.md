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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
API репликации предоставляет функции поставщика хранения сообщений MAPI для синхронизации элементов Microsoft Outlook 2013 или Microsoft Outlook 2010, русская версия между сервером и частным локальным хранилищем на основе PST, созданным для этого поставщика. 
  
> [!NOTE]
> Поставщик хранения сообщений MAPI должен реализовать API репликации в соответствии с инструкциями в области компьютера [репликации.](about-the-replication-state-machine.md) Поставщик должен использовать API только в личном хранилище, созданном для себя, а не в личных магазинах, созданных для других поставщиков, так как личные хранилища, созданные для других поставщиков, могут уже настроить собственные механизмы репликации на соответствующем сервере. Например, файл автономной папки (OST) поддерживает собственную связь репликации с сервером Microsoft Exchange. 
  
Чтобы использовать API репликации, поставщик службы хранения сообщений MAPI должен сначала открыть и завернуть локальное хранилище на основе PST, вызывая **[NSTServiceEntry.](nstserviceentry.md)** Затем поставщик может использовать основные интерфейсы API, **[IOSTX](iostxiunknown.md)** и **[IPSTX](ipstxiunknown.md)** для выполнения репликации. **IPSTX** предоставляется путем запроса [iMsgStore : IMAPIProp,](imsgstoreimapiprop.md)а **IOSTX** **[предоставляется IPSTX::GetSyncObject](ipstx-getsyncobject.md)**. 
  
## <a name="the-iostx-interface"></a>Интерфейс IOSTX

Интерфейс **IOSTX** — это основной интерфейс, который выполняет синхронизацию в API репликации. **IOSTX** перемещает локальное хранилище по ряду штатов, по мере получения информации в каждом состоянии об изменениях в локальном хранилище, а также информирования локального магазина об изменениях на сервере. API репликации также указывает множество структур данных, которые поддерживают синхронизацию. 
  
Поставщик магазина в качестве клиента для этого API использует API репликации для переноса локального хранения и перемещения по этим состояниям, внесения изменений в локальное хранилище (например, изменений в иерархии папок или добавления новых элементов) на сервер, а также получения сведений об изменениях на сервере и предоставления этих сведений интерфейсу **IOSTX.** Интерфейс **IOSTX** принимает добаво бытовую синхронизацию изменений (ICS), предоставляемую Microsoft Exchange Server. Дополнительные сведения о ICS см. в [критериях оценки ICS.](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx) С **помощью IOSTX** клиент использует ICS для отслеживания и синхронизации добавческих изменений иерархии или контента в локальном хранилище. 
  
## <a name="the-ipstx-interface"></a>Интерфейс IPSTX

 **IPSTX** и пять других **IPSTX *n* ** интерфейсов, наследуемые от **IPSTX,** предоставляют дополнительные функции, которые можно использовать при выполнении репликации через интерфейс **IOSTX.** Например, **[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)** позволяет сделать локальное хранилище эмулировать диспетчер протоколов Outlook для перенаправления исходяющих сообщений на сервер. 
  
Дополнительные сведения о переходах состояния во время репликации см. в сведениях о автомате [репликации.](about-the-replication-state-machine.md)
  
## <a name="the-replication-api"></a>API репликации

API репликации предоставляет следующие отсрочки, типы данных и интерфейсы. Пример реализации поставщика магазина для упакованных файлов личных папок (PST) см. в примере поставщика упакованных [PST-файлов.](about-the-sample-wrapped-pst-store-provider.md)
  
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
    

