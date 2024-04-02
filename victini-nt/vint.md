enum Type = byte, char, short, int, long, float, double, string
struct BitType { // 3 byte
    size: 16
    struct_prototype_map_index: 8
}

Publish {
    PublishHeader
    SinglePublishedPacket[];
}

NewStructPrototype{
    {
        
        name: char[]
        BitType
    }[]
}

PublishHeader{
    "VI": 16
    new_struct_prototypes: 
}

SinglePublishedPacket {
    start: '\xff'
    is_struct: 1
    

    end: '\x00'
}