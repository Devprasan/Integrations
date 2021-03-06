# @datafire/fantasydata_mlb_v3_stats

Client library for MLB v3 Stats

## Installation and Usage
```bash
npm install --save @datafire/fantasydata_mlb_v3_stats
```
```js
let fantasydata_mlb_v3_stats = require('@datafire/fantasydata_mlb_v3_stats').create({
  apiKeyHeader: "",
  apiKeyQuery: ""
});

fantasydata_mlb_v3_stats.TeamsAll({
  "format": ""
}).then(data => {
  console.log(data);
});
```

## Description

MLB scores, stats, and news API.

## Actions

### TeamsAll
Teams (All)


```js
fantasydata_mlb_v3_stats.TeamsAll({
  "format": ""
}, context)
```

#### Input
* input `object`
  * format **required** `string` (values: XML, JSON): Desired response format. Valid entries are <code>XML</code> or <code>JSON</code>.

#### Output
* output `array`
  * items [Team](#team)

### AreGamesInProgress
Returns <code>true</code> if there is at least one game being played at the time of the request or <code>false</code> if there are none.


```js
fantasydata_mlb_v3_stats.AreGamesInProgress({
  "format": ""
}, context)
```

#### Input
* input `object`
  * format **required** `string` (values: XML, JSON): Desired response format. Valid entries are <code>XML</code> or <code>JSON</code>.

#### Output
* output `boolean`

### BoxScore
Box Score


```js
fantasydata_mlb_v3_stats.BoxScore({
  "format": "",
  "gameid": ""
}, context)
```

#### Input
* input `object`
  * format **required** `string` (values: XML, JSON): Desired response format. Valid entries are <code>XML</code> or <code>JSON</code>.
  * gameid **required** `string`: The GameID of an MLB game.  GameIDs can be found in the Games API.  Valid entries are <code>14620</code> or <code>16905</code>

#### Output
* output [BoxScore](#boxscore)

### BoxScoresByDate
Box Scores by Date


```js
fantasydata_mlb_v3_stats.BoxScoresByDate({
  "format": "",
  "date": ""
}, context)
```

#### Input
* input `object`
  * format **required** `string` (values: XML, JSON): Desired response format. Valid entries are <code>XML</code> or <code>JSON</code>.
  * date **required** `string`: The date of the game(s).

#### Output
* output `array`
  * items [BoxScore](#boxscore)

### BoxScoresByDateDelta
Box Scores by Date Delta


```js
fantasydata_mlb_v3_stats.BoxScoresByDateDelta({
  "format": "",
  "date": "",
  "minutes": ""
}, context)
```

#### Input
* input `object`
  * format **required** `string` (values: XML, JSON): Desired response format. Valid entries are <code>XML</code> or <code>JSON</code>.
  * date **required** `string`: The date of the game(s).
  * minutes **required** `string`: Only returns player statistics that have changed in the last X minutes.  You specify how many minutes in time to go back. Valid entries are:

#### Output
* output `array`
  * items [BoxScore](#boxscore)

### CurrentSeason
Current Season


```js
fantasydata_mlb_v3_stats.CurrentSeason({
  "format": ""
}, context)
```

#### Input
* input `object`
  * format **required** `string` (values: XML, JSON): Desired response format. Valid entries are <code>XML</code> or <code>JSON</code>.

#### Output
* output [Season](#season)

### DfsSlatesByDate
DFS Slates by Date


```js
fantasydata_mlb_v3_stats.DfsSlatesByDate({
  "format": "",
  "date": ""
}, context)
```

#### Input
* input `object`
  * format **required** `string` (values: XML, JSON): Desired response format. Valid entries are <code>XML</code> or <code>JSON</code>.
  * date **required** `string`: The date of the slates.

#### Output
* output `array`
  * items [DfsSlate](#dfsslate)

### PlayerDetailsByFreeAgents
Player Details by Free Agents


```js
fantasydata_mlb_v3_stats.PlayerDetailsByFreeAgents({
  "format": ""
}, context)
```

#### Input
* input `object`
  * format **required** `string` (values: XML, JSON): Desired response format. Valid entries are <code>XML</code> or <code>JSON</code>.

#### Output
* output `array`
  * items [Player](#player)

### Schedules
Schedules


```js
fantasydata_mlb_v3_stats.Schedules({
  "format": "",
  "season": ""
}, context)
```

#### Input
* input `object`
  * format **required** `string` (values: XML, JSON): Desired response format. Valid entries are <code>XML</code> or <code>JSON</code>.
  * season **required** `string`: Year of the season (with optional season type).<br>Examples: <code>2018</code>, <code>2018PRE</code>, <code>2018POST</code>, <code>2018STAR</code>, <code>2019</code>, etc.

#### Output
* output `array`
  * items [Game](#game)

### GamesByDate
Games by Date


```js
fantasydata_mlb_v3_stats.GamesByDate({
  "format": "",
  "date": ""
}, context)
```

#### Input
* input `object`
  * format **required** `string` (values: XML, JSON): Desired response format. Valid entries are <code>XML</code> or <code>JSON</code>.
  * date **required** `string`: The date of the game(s).

#### Output
* output `array`
  * items [Game](#game)

### BatterVsPitcherStats
Batter vs. Pitcher Stats


```js
fantasydata_mlb_v3_stats.BatterVsPitcherStats({
  "format": "",
  "hitterid": "",
  "pitcherid": ""
}, context)
```

#### Input
* input `object`
  * format **required** `string` (values: XML, JSON): Desired response format. Valid entries are <code>XML</code> or <code>JSON</code>.
  * hitterid **required** `string`: Unique FantasyData Player ID.
  * pitcherid **required** `string`: Unique FantasyData Player ID.

#### Output
* output `array`
  * items [PlayerSeason](#playerseason)

### News
News


```js
fantasydata_mlb_v3_stats.News({
  "format": ""
}, context)
```

#### Input
* input `object`
  * format **required** `string` (values: XML, JSON): Desired response format. Valid entries are <code>XML</code> or <code>JSON</code>.

#### Output
* output `array`
  * items [News](#news)

### NewsByDate
News by Date


```js
fantasydata_mlb_v3_stats.NewsByDate({
  "format": "",
  "date": ""
}, context)
```

#### Input
* input `object`
  * format **required** `string` (values: XML, JSON): Desired response format. Valid entries are <code>XML</code> or <code>JSON</code>.
  * date **required** `string`: The date of the news.

#### Output
* output `array`
  * items [News](#news)

### NewsByPlayer
News by Player


```js
fantasydata_mlb_v3_stats.NewsByPlayer({
  "format": "",
  "playerid": ""
}, context)
```

#### Input
* input `object`
  * format **required** `string` (values: XML, JSON): Desired response format. Valid entries are <code>XML</code> or <code>JSON</code>.
  * playerid **required** `string`: Unique FantasyData Player ID.

#### Output
* output `array`
  * items [News](#news)

### PlayerDetailsByPlayer
Player Details by Player


```js
fantasydata_mlb_v3_stats.PlayerDetailsByPlayer({
  "format": "",
  "playerid": ""
}, context)
```

#### Input
* input `object`
  * format **required** `string` (values: XML, JSON): Desired response format. Valid entries are <code>XML</code> or <code>JSON</code>.
  * playerid **required** `string`: Unique FantasyData Player ID.

#### Output
* output [Player](#player)

### PlayerGameStatsByDate
Player Game Stats by Date


```js
fantasydata_mlb_v3_stats.PlayerGameStatsByDate({
  "format": "",
  "date": ""
}, context)
```

#### Input
* input `object`
  * format **required** `string` (values: XML, JSON): Desired response format. Valid entries are <code>XML</code> or <code>JSON</code>.
  * date **required** `string`: The date of the game(s).

#### Output
* output `array`
  * items [PlayerGame](#playergame)

### PlayerGameStatsByPlayer
Player Game Stats by Player


```js
fantasydata_mlb_v3_stats.PlayerGameStatsByPlayer({
  "format": "",
  "date": "",
  "playerid": ""
}, context)
```

#### Input
* input `object`
  * format **required** `string` (values: XML, JSON): Desired response format. Valid entries are <code>XML</code> or <code>JSON</code>.
  * date **required** `string`: The date of the game(s).
  * playerid **required** `string`: Unique FantasyData Player ID.

#### Output
* output [PlayerGame](#playergame)

### PlayerSeasonAwayStats
Player Season Away Stats


```js
fantasydata_mlb_v3_stats.PlayerSeasonAwayStats({
  "format": "",
  "season": ""
}, context)
```

#### Input
* input `object`
  * format **required** `string` (values: XML, JSON): Desired response format. Valid entries are <code>XML</code> or <code>JSON</code>.
  * season **required** `string`: Year of the season.

#### Output
* output `array`
  * items [PlayerSeason](#playerseason)

### PlayerSeasonHomeStats
Player Season Home Stats


```js
fantasydata_mlb_v3_stats.PlayerSeasonHomeStats({
  "format": "",
  "season": ""
}, context)
```

#### Input
* input `object`
  * format **required** `string` (values: XML, JSON): Desired response format. Valid entries are <code>XML</code> or <code>JSON</code>.
  * season **required** `string`: Year of the season.

#### Output
* output `array`
  * items [PlayerSeason](#playerseason)

### PlayerSeasonSplitStats
Player Season Split Stats


```js
fantasydata_mlb_v3_stats.PlayerSeasonSplitStats({
  "format": "",
  "season": "",
  "split": ""
}, context)
```

#### Input
* input `object`
  * format **required** `string` (values: XML, JSON): Desired response format. Valid entries are <code>XML</code> or <code>JSON</code>.
  * season **required** `string`: Year of the season.
  * split **required** `string` (values: L, R, S): The desired split of stats. Currently, we support vs. Left/Right/Switch handed pitchers/hitters. Possible values are: <code>L</code>, <code>R</code> and <code>S</code>

#### Output
* output `array`
  * items [PlayerSeason](#playerseason)

### PlayerSeasonStats
Player Season Stats


```js
fantasydata_mlb_v3_stats.PlayerSeasonStats({
  "format": "",
  "season": ""
}, context)
```

#### Input
* input `object`
  * format **required** `string` (values: XML, JSON): Desired response format. Valid entries are <code>XML</code> or <code>JSON</code>.
  * season **required** `string`: Year of the season.

#### Output
* output `array`
  * items [PlayerSeason](#playerseason)

### PlayerSeasonStatsByPlayer
Player Season Stats By Player


```js
fantasydata_mlb_v3_stats.PlayerSeasonStatsByPlayer({
  "format": "",
  "season": "",
  "playerid": ""
}, context)
```

#### Input
* input `object`
  * format **required** `string` (values: XML, JSON): Desired response format. Valid entries are <code>XML</code> or <code>JSON</code>.
  * season **required** `string`: Year of the season.
  * playerid **required** `string`: Unique FantasyData Player ID.

#### Output
* output [PlayerSeason](#playerseason)

### PlayerSeasonStatsByTeam
Player Season Stats by Team


```js
fantasydata_mlb_v3_stats.PlayerSeasonStatsByTeam({
  "format": "",
  "season": "",
  "team": ""
}, context)
```

#### Input
* input `object`
  * format **required** `string` (values: XML, JSON): Desired response format. Valid entries are <code>XML</code> or <code>JSON</code>.
  * season **required** `string`: Year of the season.
  * team **required** `string`: The abbreviation of the requested team.

#### Output
* output `array`
  * items [PlayerSeason](#playerseason)

### PlayerSeasonStatsSplitByTeam
Player Season Stats Split By Team


```js
fantasydata_mlb_v3_stats.PlayerSeasonStatsSplitByTeam({
  "format": "",
  "season": ""
}, context)
```

#### Input
* input `object`
  * format **required** `string` (values: XML, JSON): Desired response format. Valid entries are <code>XML</code> or <code>JSON</code>.
  * season **required** `string`: Year of the season.

#### Output
* output `array`
  * items [PlayerSeason](#playerseason)

### PlayerDetailsByActive
Player Details by Active


```js
fantasydata_mlb_v3_stats.PlayerDetailsByActive({
  "format": ""
}, context)
```

#### Input
* input `object`
  * format **required** `string` (values: XML, JSON): Desired response format. Valid entries are <code>XML</code> or <code>JSON</code>.

#### Output
* output `array`
  * items [Player](#player)

### PlayersByTeam
Players by Team


```js
fantasydata_mlb_v3_stats.PlayersByTeam({
  "format": "",
  "team": ""
}, context)
```

#### Input
* input `object`
  * format **required** `string` (values: XML, JSON): Desired response format. Valid entries are <code>XML</code> or <code>JSON</code>.
  * team **required** `string`: The abbreviation of the requested team.

#### Output
* output `array`
  * items [Player](#player)

### Stadiums
Stadiums


```js
fantasydata_mlb_v3_stats.Stadiums({
  "format": ""
}, context)
```

#### Input
* input `object`
  * format **required** `string` (values: xml, json): Desired response format. Valid entries are <code>XML</code> or <code>JSON</code>.

#### Output
* output `array`
  * items [Stadium](#stadium)

### Standings
Standings


```js
fantasydata_mlb_v3_stats.Standings({
  "format": "",
  "season": ""
}, context)
```

#### Input
* input `object`
  * format **required** `string` (values: XML, JSON): Desired response format. Valid entries are <code>XML</code> or <code>JSON</code>.
  * season **required** `string`: Year of the season.

#### Output
* output `array`
  * items [Standing](#standing)

### TeamGameStatsByDate
Team Game Stats by Date


```js
fantasydata_mlb_v3_stats.TeamGameStatsByDate({
  "format": "",
  "date": ""
}, context)
```

#### Input
* input `object`
  * format **required** `string` (values: XML, JSON): Desired response format. Valid entries are <code>XML</code> or <code>JSON</code>.
  * date **required** `string`: The date of the game(s).

#### Output
* output `array`
  * items [TeamGame](#teamgame)

### TeamHittingVsStartingPitcher
Team Hitting vs. Starting Pitcher


```js
fantasydata_mlb_v3_stats.TeamHittingVsStartingPitcher({
  "format": "",
  "gameid": "",
  "team": ""
}, context)
```

#### Input
* input `object`
  * format **required** `string` (values: XML, JSON): Desired response format. Valid entries are <code>XML</code> or <code>JSON</code>.
  * gameid **required** `string`: The GameID of an MLB game.  GameIDs can be found in the Games API.  Valid entries are <code>14620</code> or <code>16905</code>
  * team **required** `string`: The abbreviation of the requested team.

#### Output
* output `array`
  * items [PlayerSeason](#playerseason)

### TeamSeasonStats
Team Season Stats


```js
fantasydata_mlb_v3_stats.TeamSeasonStats({
  "format": "",
  "season": ""
}, context)
```

#### Input
* input `object`
  * format **required** `string` (values: XML, JSON): Desired response format. Valid entries are <code>XML</code> or <code>JSON</code>.
  * season **required** `string`: Year of the season.

#### Output
* output `array`
  * items [TeamSeason](#teamseason)

### TeamsActive
Teams (Active)


```js
fantasydata_mlb_v3_stats.TeamsActive({
  "format": ""
}, context)
```

#### Input
* input `object`
  * format **required** `string` (values: XML, JSON): Desired response format. Valid entries are <code>XML</code> or <code>JSON</code>.

#### Output
* output `array`
  * items [Team](#team)



## Definitions

### BoxScore
* BoxScore `object`
  * Game [Game](#game)
  * Innings `array`
    * items [Inning](#inning)
  * PlayerGames `array`
    * items [PlayerGame](#playergame)
  * TeamGames `array`
    * items [TeamGame](#teamgame)

### DfsSlate
* DfsSlate `object`
  * DfsSlateGames `array`
    * items [DfsSlateGame](#dfsslategame)
  * DfsSlatePlayers `array`
    * items [DfsSlatePlayer](#dfsslateplayer)
  * IsMultiDaySlate `boolean`
  * NumberOfGames `integer`
  * Operator `string`
  * OperatorDay `string`
  * OperatorGameType `string`
  * OperatorName `string`
  * OperatorSlateID `integer`
  * OperatorStartTime `string`
  * RemovedByOperator `boolean`
  * SlateID `integer`

### DfsSlateGame
* DfsSlateGame `object`
  * Game [Game](#game)
  * GameID `integer`
  * OperatorGameID `integer`
  * RemovedByOperator `boolean`
  * SlateGameID `integer`
  * SlateID `integer`

### DfsSlatePlayer
* DfsSlatePlayer `object`
  * OperatorPlayerID `string`
  * OperatorPlayerName `string`
  * OperatorPosition `string`
  * OperatorRosterSlots `array`
    * items `string`
  * OperatorSalary `integer`
  * OperatorSlatePlayerID `string`
  * PlayerGameProjectionStatID `integer`
  * PlayerID `integer`
  * RemovedByOperator `boolean`
  * SlateGameID `integer`
  * SlateID `integer`
  * SlatePlayerID `integer`

### Game
* Game `object`
  * Attendance `integer`
  * AwayTeam `string`
  * AwayTeamErrors `integer`
  * AwayTeamHits `integer`
  * AwayTeamID `integer`
  * AwayTeamMoneyLine `integer`
  * AwayTeamProbablePitcherID `integer`
  * AwayTeamRuns `integer`
  * AwayTeamStartingPitcher `string`
  * AwayTeamStartingPitcherID `integer`
  * Balls `integer`
  * Channel `string`
  * CurrentHitter `string`
  * CurrentHitterID `integer`
  * CurrentHittingTeamID `integer`
  * CurrentPitcher `string`
  * CurrentPitcherID `integer`
  * CurrentPitchingTeamID `integer`
  * DateTime `string`
  * Day `string`
  * DueUpHitterID1 `integer`
  * DueUpHitterID2 `integer`
  * DueUpHitterID3 `integer`
  * ForecastDescription `string`
  * ForecastTempHigh `integer`
  * ForecastTempLow `integer`
  * ForecastWindChill `integer`
  * ForecastWindDirection `integer`
  * ForecastWindSpeed `integer`
  * GameID `integer`
  * GlobalAwayTeamID `integer`
  * GlobalGameID `integer`
  * GlobalHomeTeamID `integer`
  * HomeTeam `string`
  * HomeTeamErrors `integer`
  * HomeTeamHits `integer`
  * HomeTeamID `integer`
  * HomeTeamMoneyLine `integer`
  * HomeTeamProbablePitcherID `integer`
  * HomeTeamRuns `integer`
  * HomeTeamStartingPitcher `string`
  * HomeTeamStartingPitcherID `integer`
  * Inning `integer`
  * InningHalf `string`
  * IsClosed `boolean`
  * LastPlay `string`
  * LosingPitcher `string`
  * LosingPitcherID `integer`
  * Outs `integer`
  * OverUnder `number`
  * PointSpread `number`
  * PointSpreadAwayTeamMoneyLine `integer`
  * PointSpreadHomeTeamMoneyLine `integer`
  * RescheduledFromGameID `integer`
  * RescheduledGameID `integer`
  * RunnerOnFirst `boolean`
  * RunnerOnSecond `boolean`
  * RunnerOnThird `boolean`
  * SavingPitcher `string`
  * SavingPitcherID `integer`
  * Season `integer`
  * SeasonType `integer`
  * StadiumID `integer`
  * Status `string`
  * Strikes `integer`
  * Updated `string`
  * WinningPitcher `string`
  * WinningPitcherID `integer`

### Inning
* Inning `object`
  * AwayTeamRuns `integer`
  * GameID `integer`
  * HomeTeamRuns `integer`
  * InningID `integer`
  * InningNumber `integer`

### News
* News `object`
  * Author `string`
  * Categories `string`
  * Content `string`
  * NewsID `integer`
  * PlayerID `integer`
  * PlayerID2 `integer`
  * Source `string`
  * Team `string`
  * Team2 `string`
  * TeamID `integer`
  * TeamID2 `integer`
  * TermsOfUse `string`
  * TimeAgo `string`
  * Title `string`
  * Updated `string`
  * Url `string`

### Player
* Player `object`
  * BatHand `string`
  * BirthCity `string`
  * BirthCountry `string`
  * BirthDate `string`
  * BirthState `string`
  * College `string`
  * DraftKingsName `string`
  * DraftKingsPlayerID `integer`
  * Experience `string`
  * FanDuelName `string`
  * FanDuelPlayerID `integer`
  * FantasyAlarmPlayerID `integer`
  * FantasyDraftName `string`
  * FantasyDraftPlayerID `integer`
  * FirstName `string`
  * GlobalTeamID `integer`
  * Height `integer`
  * HighSchool `string`
  * InjuryBodyPart `string`
  * InjuryNotes `string`
  * InjuryStartDate `string`
  * InjuryStatus `string`
  * Jersey `integer`
  * LastName `string`
  * MLBAMID `integer`
  * PhotoUrl `string`
  * PlayerID `integer`
  * Position `string`
  * PositionCategory `string`
  * ProDebut `string`
  * RotoWirePlayerID `integer`
  * RotoworldPlayerID `integer`
  * Salary `integer`
  * SportRadarPlayerID `string`
  * SportsDataID `string`
  * SportsDirectPlayerID `integer`
  * StatsPlayerID `integer`
  * Status `string`
  * Team `string`
  * TeamID `integer`
  * ThrowHand `string`
  * UpcomingGameID `integer`
  * Weight `integer`
  * XmlTeamPlayerID `integer`
  * YahooName `string`
  * YahooPlayerID `integer`

### PlayerGame
* PlayerGame `object`
  * AtBats `number`
  * BallsInPlay `number`
  * BattingAverage `number`
  * BattingAverageOnBallsInPlay `number`
  * BattingOrder `integer`
  * BattingOrderConfirmed `boolean`
  * CaughtStealing `number`
  * DateTime `string`
  * Day `string`
  * DoublePlays `number`
  * Doubles `number`
  * DraftKingsPosition `string`
  * DraftKingsSalary `integer`
  * EarnedRunAverage `number`
  * Errors `number`
  * FanDuelPosition `string`
  * FanDuelSalary `integer`
  * FantasyDataSalary `integer`
  * FantasyDraftPosition `string`
  * FantasyDraftSalary `integer`
  * FantasyPoints `number`
  * FantasyPointsDraftKings `number`
  * FantasyPointsFanDuel `number`
  * FantasyPointsFantasyDraft `number`
  * FantasyPointsYahoo `number`
  * FieldingIndependentPitching `number`
  * FlyOuts `number`
  * GameID `integer`
  * Games `integer`
  * GlobalGameID `integer`
  * GlobalOpponentID `integer`
  * GlobalTeamID `integer`
  * GrandSlams `number`
  * GroundIntoDoublePlay `number`
  * GroundOuts `number`
  * HitByPitch `number`
  * Hits `number`
  * HomeOrAway `string`
  * HomeRuns `number`
  * InjuryBodyPart `string`
  * InjuryNotes `string`
  * InjuryStartDate `string`
  * InjuryStatus `string`
  * InningsPitchedDecimal `number`
  * InningsPitchedFull `number`
  * InningsPitchedOuts `number`
  * IntentionalWalks `number`
  * IsGameOver `boolean`
  * IsolatedPower `number`
  * LeftOnBase `number`
  * LineOuts `number`
  * Losses `number`
  * Name `string`
  * OnBasePercentage `number`
  * OnBasePlusSlugging `number`
  * Opponent `string`
  * OpponentID `integer`
  * OpponentPositionRank `integer`
  * OpponentRank `integer`
  * Outs `number`
  * PitchesSeen `number`
  * PitchesThrown `number`
  * PitchesThrownStrikes `number`
  * PitchingBallsInPlay `number`
  * PitchingBattingAverageAgainst `number`
  * PitchingBattingAverageOnBallsInPlay `number`
  * PitchingBlownSaves `number`
  * PitchingCatchersInterference `number`
  * PitchingCompleteGames `number`
  * PitchingDoublePlays `number`
  * PitchingDoubles `number`
  * PitchingEarnedRuns `number`
  * PitchingFlyOuts `number`
  * PitchingGrandSlams `number`
  * PitchingGroundIntoDoublePlay `number`
  * PitchingGroundOuts `number`
  * PitchingHitByPitch `number`
  * PitchingHits `number`
  * PitchingHolds `number`
  * PitchingHomeRuns `number`
  * PitchingInningStarted `integer`
  * PitchingIntentionalWalks `number`
  * PitchingLineOuts `number`
  * PitchingNoHitters `number`
  * PitchingOnBasePercentage `number`
  * PitchingOnBasePlusSlugging `number`
  * PitchingPerfectGames `number`
  * PitchingPlateAppearances `number`
  * PitchingPopOuts `number`
  * PitchingQualityStarts `number`
  * PitchingReachedOnError `number`
  * PitchingRuns `number`
  * PitchingSacrificeFlies `number`
  * PitchingSacrifices `number`
  * PitchingShutOuts `number`
  * PitchingSingles `number`
  * PitchingSluggingPercentage `number`
  * PitchingStrikeouts `number`
  * PitchingStrikeoutsPerNineInnings `number`
  * PitchingTotalBases `number`
  * PitchingTriples `number`
  * PitchingWalks `number`
  * PitchingWalksPerNineInnings `number`
  * PitchingWeightedOnBasePercentage `number`
  * PlateAppearances `number`
  * PlayerID `integer`
  * PopOuts `number`
  * Position `string`
  * PositionCategory `string`
  * ReachedOnError `number`
  * Runs `number`
  * RunsBattedIn `number`
  * SacrificeFlies `number`
  * Sacrifices `number`
  * Saves `number`
  * Season `integer`
  * SeasonType `integer`
  * Singles `number`
  * SluggingPercentage `number`
  * Started `integer`
  * StatID `integer`
  * StolenBases `number`
  * Strikeouts `number`
  * SubstituteBattingOrder `integer`
  * SubstituteBattingOrderSequence `integer`
  * Team `string`
  * TeamID `integer`
  * TotalBases `number`
  * TotalOutsPitched `number`
  * Triples `number`
  * Updated `string`
  * Walks `number`
  * WalksHitsPerInningsPitched `number`
  * WeightedOnBasePercentage `number`
  * Wins `number`
  * YahooPosition `string`
  * YahooSalary `integer`

### PlayerSeason
* PlayerSeason `object`
  * AtBats `number`
  * AverageDraftPosition `number`
  * BallsInPlay `number`
  * BattingAverage `number`
  * BattingAverageOnBallsInPlay `number`
  * BattingOrder `integer`
  * BattingOrderConfirmed `boolean`
  * CaughtStealing `number`
  * DoublePlays `number`
  * Doubles `number`
  * EarnedRunAverage `number`
  * Errors `number`
  * FantasyPoints `number`
  * FantasyPointsDraftKings `number`
  * FantasyPointsFanDuel `number`
  * FantasyPointsFantasyDraft `number`
  * FantasyPointsYahoo `number`
  * FieldingIndependentPitching `number`
  * FlyOuts `number`
  * Games `integer`
  * GlobalTeamID `integer`
  * GrandSlams `number`
  * GroundIntoDoublePlay `number`
  * GroundOuts `number`
  * HitByPitch `number`
  * Hits `number`
  * HomeRuns `number`
  * InningsPitchedDecimal `number`
  * InningsPitchedFull `number`
  * InningsPitchedOuts `number`
  * IntentionalWalks `number`
  * IsolatedPower `number`
  * LeftOnBase `number`
  * LineOuts `number`
  * Losses `number`
  * Name `string`
  * OnBasePercentage `number`
  * OnBasePlusSlugging `number`
  * Outs `number`
  * PitchesSeen `number`
  * PitchesThrown `number`
  * PitchesThrownStrikes `number`
  * PitchingBallsInPlay `number`
  * PitchingBattingAverageAgainst `number`
  * PitchingBattingAverageOnBallsInPlay `number`
  * PitchingBlownSaves `number`
  * PitchingCatchersInterference `number`
  * PitchingCompleteGames `number`
  * PitchingDoublePlays `number`
  * PitchingDoubles `number`
  * PitchingEarnedRuns `number`
  * PitchingFlyOuts `number`
  * PitchingGrandSlams `number`
  * PitchingGroundIntoDoublePlay `number`
  * PitchingGroundOuts `number`
  * PitchingHitByPitch `number`
  * PitchingHits `number`
  * PitchingHolds `number`
  * PitchingHomeRuns `number`
  * PitchingInningStarted `integer`
  * PitchingIntentionalWalks `number`
  * PitchingLineOuts `number`
  * PitchingNoHitters `number`
  * PitchingOnBasePercentage `number`
  * PitchingOnBasePlusSlugging `number`
  * PitchingPerfectGames `number`
  * PitchingPlateAppearances `number`
  * PitchingPopOuts `number`
  * PitchingQualityStarts `number`
  * PitchingReachedOnError `number`
  * PitchingRuns `number`
  * PitchingSacrificeFlies `number`
  * PitchingSacrifices `number`
  * PitchingShutOuts `number`
  * PitchingSingles `number`
  * PitchingSluggingPercentage `number`
  * PitchingStrikeouts `number`
  * PitchingStrikeoutsPerNineInnings `number`
  * PitchingTotalBases `number`
  * PitchingTriples `number`
  * PitchingWalks `number`
  * PitchingWalksPerNineInnings `number`
  * PitchingWeightedOnBasePercentage `number`
  * PlateAppearances `number`
  * PlayerID `integer`
  * PopOuts `number`
  * Position `string`
  * PositionCategory `string`
  * ReachedOnError `number`
  * Runs `number`
  * RunsBattedIn `number`
  * SacrificeFlies `number`
  * Sacrifices `number`
  * Saves `number`
  * Season `integer`
  * SeasonType `integer`
  * Singles `number`
  * SluggingPercentage `number`
  * Started `integer`
  * StatID `integer`
  * StolenBases `number`
  * Strikeouts `number`
  * SubstituteBattingOrder `integer`
  * SubstituteBattingOrderSequence `integer`
  * Team `string`
  * TeamID `integer`
  * TotalBases `number`
  * TotalOutsPitched `number`
  * Triples `number`
  * Updated `string`
  * Walks `number`
  * WalksHitsPerInningsPitched `number`
  * WeightedOnBasePercentage `number`
  * Wins `number`

### Season
* Season `object`
  * ApiSeason `string`
  * PostSeasonStartDate `string`
  * RegularSeasonStartDate `string`
  * Season `integer`
  * SeasonType `string`

### Stadium
* Stadium `object`
  * Active `boolean`
  * Altitude `integer`
  * Capacity `integer`
  * CenterField `integer`
  * City `string`
  * Country `string`
  * GeoLat `number`
  * GeoLong `number`
  * HomePlateDirection `integer`
  * LeftCenterField `integer`
  * LeftField `integer`
  * MidLeftCenterField `integer`
  * MidLeftField `integer`
  * MidRightCenterField `integer`
  * MidRightField `integer`
  * Name `string`
  * RightCenterField `integer`
  * RightField `integer`
  * StadiumID `integer`
  * State `string`
  * Surface `string`
  * Type `string`

### Standing
* Standing `object`
  * AwayLosses `integer`
  * AwayWins `integer`
  * City `string`
  * DayLosses `integer`
  * DayWins `integer`
  * Division `string`
  * DivisionLosses `integer`
  * DivisionWins `integer`
  * GamesBehind `number`
  * HomeLosses `integer`
  * HomeWins `integer`
  * Key `string`
  * LastTenGamesLosses `integer`
  * LastTenGamesWins `integer`
  * League `string`
  * Losses `integer`
  * Name `string`
  * NightLosses `integer`
  * NightWins `integer`
  * Percentage `number`
  * Season `integer`
  * SeasonType `integer`
  * Streak `string`
  * TeamID `integer`
  * WildCardGamesBehind `number`
  * WildCardRank `integer`
  * Wins `integer`

### Team
* Team `object`
  * Active `boolean`
  * City `string`
  * Division `string`
  * GlobalTeamID `integer`
  * League `string`
  * Name `string`
  * PrimaryColor `string`
  * QuaternaryColor `string`
  * SecondaryColor `string`
  * StadiumID `integer`
  * TeamID `integer`
  * TertiaryColor `string`
  * WikipediaLogoUrl `string`
  * WikipediaWordMarkUrl `string`
  * [Key] `string`

### TeamGame
* TeamGame `object`
  * AtBats `number`
  * BallsInPlay `number`
  * BattingAverage `number`
  * BattingAverageOnBallsInPlay `number`
  * BattingOrderConfirmed `boolean`
  * CaughtStealing `number`
  * DateTime `string`
  * Day `string`
  * DoublePlays `number`
  * Doubles `number`
  * EarnedRunAverage `number`
  * Errors `number`
  * FantasyPoints `number`
  * FantasyPointsDraftKings `number`
  * FantasyPointsFanDuel `number`
  * FantasyPointsFantasyDraft `number`
  * FantasyPointsYahoo `number`
  * FieldingIndependentPitching `number`
  * FlyOuts `number`
  * GameID `integer`
  * Games `integer`
  * GlobalGameID `integer`
  * GlobalOpponentID `integer`
  * GlobalTeamID `integer`
  * GrandSlams `number`
  * GroundIntoDoublePlay `number`
  * GroundOuts `number`
  * HitByPitch `number`
  * Hits `number`
  * HomeOrAway `string`
  * HomeRuns `number`
  * InningsPitchedDecimal `number`
  * InningsPitchedFull `number`
  * InningsPitchedOuts `number`
  * IntentionalWalks `number`
  * IsGameOver `boolean`
  * IsolatedPower `number`
  * LeftOnBase `number`
  * LineOuts `number`
  * Losses `number`
  * Name `string`
  * OnBasePercentage `number`
  * OnBasePlusSlugging `number`
  * Opponent `string`
  * OpponentID `integer`
  * Outs `number`
  * PitchesSeen `number`
  * PitchesThrown `number`
  * PitchesThrownStrikes `number`
  * PitchingBallsInPlay `number`
  * PitchingBattingAverageAgainst `number`
  * PitchingBattingAverageOnBallsInPlay `number`
  * PitchingBlownSaves `number`
  * PitchingCatchersInterference `number`
  * PitchingCompleteGames `number`
  * PitchingDoublePlays `number`
  * PitchingDoubles `number`
  * PitchingEarnedRuns `number`
  * PitchingFlyOuts `number`
  * PitchingGrandSlams `number`
  * PitchingGroundIntoDoublePlay `number`
  * PitchingGroundOuts `number`
  * PitchingHitByPitch `number`
  * PitchingHits `number`
  * PitchingHolds `number`
  * PitchingHomeRuns `number`
  * PitchingInningStarted `integer`
  * PitchingIntentionalWalks `number`
  * PitchingLineOuts `number`
  * PitchingNoHitters `number`
  * PitchingOnBasePercentage `number`
  * PitchingOnBasePlusSlugging `number`
  * PitchingPerfectGames `number`
  * PitchingPlateAppearances `number`
  * PitchingPopOuts `number`
  * PitchingQualityStarts `number`
  * PitchingReachedOnError `number`
  * PitchingRuns `number`
  * PitchingSacrificeFlies `number`
  * PitchingSacrifices `number`
  * PitchingShutOuts `number`
  * PitchingSingles `number`
  * PitchingSluggingPercentage `number`
  * PitchingStrikeouts `number`
  * PitchingStrikeoutsPerNineInnings `number`
  * PitchingTotalBases `number`
  * PitchingTriples `number`
  * PitchingWalks `number`
  * PitchingWalksPerNineInnings `number`
  * PitchingWeightedOnBasePercentage `number`
  * PlateAppearances `number`
  * PopOuts `number`
  * ReachedOnError `number`
  * Runs `number`
  * RunsBattedIn `number`
  * SacrificeFlies `number`
  * Sacrifices `number`
  * Saves `number`
  * Season `integer`
  * SeasonType `integer`
  * Singles `number`
  * SluggingPercentage `number`
  * StatID `integer`
  * StolenBases `number`
  * Strikeouts `number`
  * SubstituteBattingOrder `integer`
  * SubstituteBattingOrderSequence `integer`
  * Team `string`
  * TeamID `integer`
  * TotalBases `number`
  * TotalOutsPitched `number`
  * Triples `number`
  * Updated `string`
  * Walks `number`
  * WalksHitsPerInningsPitched `number`
  * WeightedOnBasePercentage `number`
  * Wins `number`

### TeamSeason
* TeamSeason `object`
  * AtBats `number`
  * BallsInPlay `number`
  * BattingAverage `number`
  * BattingAverageOnBallsInPlay `number`
  * BattingOrderConfirmed `boolean`
  * CaughtStealing `number`
  * DoublePlays `number`
  * Doubles `number`
  * EarnedRunAverage `number`
  * Errors `number`
  * FantasyPoints `number`
  * FantasyPointsDraftKings `number`
  * FantasyPointsFanDuel `number`
  * FantasyPointsFantasyDraft `number`
  * FantasyPointsYahoo `number`
  * FieldingIndependentPitching `number`
  * FlyOuts `number`
  * Games `integer`
  * GlobalTeamID `integer`
  * GrandSlams `number`
  * GroundIntoDoublePlay `number`
  * GroundOuts `number`
  * HitByPitch `number`
  * Hits `number`
  * HomeRuns `number`
  * InningsPitchedDecimal `number`
  * InningsPitchedFull `number`
  * InningsPitchedOuts `number`
  * IntentionalWalks `number`
  * IsolatedPower `number`
  * LeftOnBase `number`
  * LineOuts `number`
  * Losses `number`
  * Name `string`
  * OnBasePercentage `number`
  * OnBasePlusSlugging `number`
  * Outs `number`
  * PitchesSeen `number`
  * PitchesThrown `number`
  * PitchesThrownStrikes `number`
  * PitchingBallsInPlay `number`
  * PitchingBattingAverageAgainst `number`
  * PitchingBattingAverageOnBallsInPlay `number`
  * PitchingBlownSaves `number`
  * PitchingCatchersInterference `number`
  * PitchingCompleteGames `number`
  * PitchingDoublePlays `number`
  * PitchingDoubles `number`
  * PitchingEarnedRuns `number`
  * PitchingFlyOuts `number`
  * PitchingGrandSlams `number`
  * PitchingGroundIntoDoublePlay `number`
  * PitchingGroundOuts `number`
  * PitchingHitByPitch `number`
  * PitchingHits `number`
  * PitchingHolds `number`
  * PitchingHomeRuns `number`
  * PitchingInningStarted `integer`
  * PitchingIntentionalWalks `number`
  * PitchingLineOuts `number`
  * PitchingNoHitters `number`
  * PitchingOnBasePercentage `number`
  * PitchingOnBasePlusSlugging `number`
  * PitchingPerfectGames `number`
  * PitchingPlateAppearances `number`
  * PitchingPopOuts `number`
  * PitchingQualityStarts `number`
  * PitchingReachedOnError `number`
  * PitchingRuns `number`
  * PitchingSacrificeFlies `number`
  * PitchingSacrifices `number`
  * PitchingShutOuts `number`
  * PitchingSingles `number`
  * PitchingSluggingPercentage `number`
  * PitchingStrikeouts `number`
  * PitchingStrikeoutsPerNineInnings `number`
  * PitchingTotalBases `number`
  * PitchingTriples `number`
  * PitchingWalks `number`
  * PitchingWalksPerNineInnings `number`
  * PitchingWeightedOnBasePercentage `number`
  * PlateAppearances `number`
  * PopOuts `number`
  * ReachedOnError `number`
  * Runs `number`
  * RunsBattedIn `number`
  * SacrificeFlies `number`
  * Sacrifices `number`
  * Saves `number`
  * Season `integer`
  * SeasonType `integer`
  * Singles `number`
  * SluggingPercentage `number`
  * StatID `integer`
  * StolenBases `number`
  * Strikeouts `number`
  * SubstituteBattingOrder `integer`
  * SubstituteBattingOrderSequence `integer`
  * Team `string`
  * TeamID `integer`
  * TotalBases `number`
  * TotalOutsPitched `number`
  * Triples `number`
  * Updated `string`
  * Walks `number`
  * WalksHitsPerInningsPitched `number`
  * WeightedOnBasePercentage `number`
  * Wins `number`


