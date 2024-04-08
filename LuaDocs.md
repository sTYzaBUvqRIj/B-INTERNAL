# Lua documentations for Growtopia Internal - bothaxyt

## This documentation is for Android (Last updated 4/8/24)
### Functions
```lua
Sleep(int milliseconds) -- Sleep for milliseconds
RunThread(function func [, ...]) -- Run new thread

LogToConsole(string text) -- Display text to Growtopia console

SendPacket(int type, string text) -- Send text packet to server
SendPacketRaw(bool client, TankPacket packet) -- Send raw packet. adjust client to false if you want send to server
SendVariantList(VariantList var [, netid][, delay]) -- Call variantList function

SendWorldTouch(float x, float y [, bool down]) -- Send world touch
SendWorldTouch(ImVec2 pos [, bool down]) -- Same as above but using ImVec2

RequestJoinWorld(string worldName) -- Warp to desired world name
```

### Miscellaneous
```lua
bool FindPath(int tile_x, int tile_y) -- Find path
bool CheckPath(int tile_x, int tile_y) -- Are there any path to desired destination?

uint32 Hash32(string str) -- Proton hash 32 byte
uint64 Hash64(string str) -- Proton hash 64 byte

int[] GetClothing([int netid]) -- Get player clothing. Default netid = local player netid
void SetClothing(int bodyPart, int item_id [, int netid]) -- Set clothing to player. Default netid = local player
void SetItemSelected(int item_id) -- Set current selected item in backpack
string GetScriptPath() -- Get script directory path

Response MakeRequest(string url [, string method][, table options][, string post_fields][, int connection_time_out]) -- Make request
```

### Getter
```lua
WorldCamera GetCamera()
ENetClient GetClient()
InventoryItem[] GetInventory() -- Get table list of all item in the inventory

ItemInfo GetItemInfo(int id)
ItemInfo GetItemInfo(string itemFullName)
ItemInfo[] GetItemInfoList() -- Get all item info in the items.dat... beware laggy

NetAvatar GetLocal()

ClientNPC GetNPC(int id) -- Get npc by id
ClientNPC[] GetNPCList() -- Get all npcs in the world

WorldObject[] GetObjectList()

PlayerItems GetPlayerItems()

NetAvatar GetPlayer(int netid) -- Get player by netid
NetAvatar[] GetPlayerList() -- Get all player info in the world

Tile GetTile(int x, int y)
Tile[] GetTiles() -- ...

World GetWorld()
```
